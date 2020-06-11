# JS

## 一、JS简介
### 01. JS历史
>1）JavaScript 诞生于 1995 年。NetSpace发布Netspace Navigator2浏览器，提供了免费开发工具LiveScript，设计的主要目的是处理以前由服务器端语言负责的一些输入验证操作。在人们普遍使用电话拔号上网的年代,能够在客户端完成一些基本的验证任务绝对很不容易。因为Java流行，所以改名为JavaScript。这个就是JavaScript1.0版本。

>2）因为JavaScript很受欢迎，Netspace Navigator3浏览器发布了JavaScript1.1版本。不久IE3也加入的脚本编程的功能，为了避免纠纷，命名为JScript。

>3）1997年，ECMA以JavaScript1.1为基础制定了脚本语言标准：ECMA-262，并命名为ECMAScript。浏览器厂商使用ECMAScript作为各自的JavaScript实现的规范标准。

### 02.ECMAScript
> 1997年，ECMA发布262号标准文件（ECMA-262）第一版，规定了脚本语言的实现标准，并将这种标准命名为ECMAScript，这个就是ES1.0版本。ECMAScript是JavaScript语言的规范标准，JavaScript是ECMAScript的一种实现方式。在一些语境中是可以互换的。

### 03.ECMAScript版本
>1）1998年6月， ECMAScriysxbzx      pt2.0版发布 
>2）1990年12月， ECMAScript3.0版发布，并成为 JavaScript的通用标准，获得广泛支持

>3）2007年10月， ECMAScript4.0版草案发布，对3.0版做了大幅升级。由于4.0版的目标过于激进各方对于是否通过这个标准产生了严重分歧，2008年7月，ECMA中止ECMAScript4.0的开发，将其中涉及现有功能改善的一小部分发布为ECMAScript3.1.不久， ECMAScript3.1改名为 ECMAScript5

>4）2009年12月， ECMAScrip5.0版正式发布

>5）2011年6月， ECMAScript 5.1版发布

>6）2013年12月， ECMAScrip6版草案发布

>7）2015年6月， ECMAScript6发布正式版本，并更名为 ECMAScript2015. Mozilla在这个标准的基础上推出了 JavaScript2.0

>8）从此以后， JavaScript开始以年份命名，新版本将按照“ ECMAScript+年份”的形式发布。目前最新版本为 ECMAScript2019,于2019年7月正式发布

### 04.JS构成
完整的JS由一下几个构成
1）ECMAScript：语言核心部分
2）文档对象模型（DOM）网页文档操作标准，HTML应用程序编程接口（API），DOM把整个文档映射成一个树形节点结构，方便JS脚本快速访问和操作。
3）浏览器对象模型（BOM） 客户端和浏览器窗口的操作基础，使用BOM可以对浏览器窗口进行访问和操作，如移动窗口，访问历史记录等等，没有规范，但是所有浏览器默认支持

### 05.为什么学习JS
- 所有主流浏览器都支持 JavaScript。
- 目前，全世界大部分网页都使用 JavaScript。
- 它可以让网页呈现各种动态效果。
- 做为一个 Web 开发师，如果你想提供漂亮的网页、令用户满意的上网体验，JavaScript 是必不可少的工具

>曾经由一段对话：
<img src='https://upload-images.jianshu.io/upload_images/3532891-82cc75e2649062cf.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240'>

>但是JS之父说：any application that can be written in JavaScript, 
will eventually be written in JavaScript
>比如：<img src=https://upload-images.jianshu.io/upload_images/3532891-52bbd1118cf170e6.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240>
<img src=https://upload-images.jianshu.io/upload_images/3532891-63f563ff13579f98.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240>
<img src=https://upload-images.jianshu.io/upload_images/3532891-b1fe603d94166d4a.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240>
<img src=https://upload-images.jianshu.io/upload_images/3532891-ed0a7d7e74ad9554.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240>
<img src=https://upload-images.jianshu.io/upload_images/3532891-1bf62f6dded85ec8.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240>

>最后来一个JS总结：<img src=https://upload-images.jianshu.io/upload_images/3532891-bba45d861677866f.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240>

### 06.JavaScript 概念

JavaScript是一种直译式脚本语言，是一种动态类型、弱类型、基于原型的语言，内置支持类型。它的解释器被称为JavaScript引擎，为浏览器的一部分，广泛用于客户端的脚本语言，在HTML网页上使用，用来给HTML网页增加动态功能。

### 07.JavaScript 概念解析

- 直译式：它不需要经过编译器先行编译为机器码，之后直接在 CPU 中运行。直译式语言需要通过解释器，在运行期动态直译。
- 脚本语言： JavaScript是在程序的运行过程中逐行进行解释，只在被调用时进行解释或编译。
- 动态类型：变量使用之前不需要类型声明，通常变量的类型是被赋值的那个值的类型。
- 弱类型：数据类型可以被忽略的语言。它与强类型定义语言相反, 一个变量可以赋不同数据类型的值
- 基于原型：只有对象,没有类;对象继承对象,而不是类继承类。“原型对象”是基于原型语言的核心概念。原型对象是新对象的模板，它将自身的属性共享给新对象。一个对象不但可以享有自己创建时和运行时定义的属性，而且可以享有原型对象的属性


## 二、JS的初步使用
### 01.script的引入
#### 1）`<script>`标签
>向 HTML 页面中插入 JavaScript 的主要方法,就是使用`<script>`元素 
按照传统的做法,所有`<script>`元素都应该放在页面的`<head>`元素中 
但是现在脚本一般都写在 body 元素紧接着关标签之上
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>JS的引入</title>
</head>
<body>
    <script>
        alert(1);
    </script>
    <script src="./demo1.js"></script>
</body>
</html>
```

#### 2）`<script>`元素 引入位置：
>可能你看到过JavaScript的其他引入语句，或者放在head标签中的JavaScript代码。作为最佳实践，我们会在关闭body标签前引入JavaScript代码。这样浏览器就会在加载脚本之前解析和显示HTML，有利于提升页面的性能

#### 3）`<script> `元素属性 
src :可选。表示包含要执行代码的外部文件。 
type :可选 一般为 text/javascript。现代浏览器默认脚本类型是JavaScript，因此可以省略type

#### 4）外部JS文件
JS程序不仅可以直接写在HTML文档中，也可以放在JavaScript文件中。后缀名是.js。使用任何文本编辑器都可以编辑

JS文件不能够单独运行，需要使用 `<script>`标签导入到网页中。

定义src树形的`<script>`标签不应该再含有JavaScript代码，否则则只会下载并执行外部JavaScript文件，嵌入代码被忽略。

#### 5）JS执行时机
浏览器解析HTML文档的时候，将根据文档流从上倒下逐行解析和显示。JS是HTML组成的一部分，因此JS脚本的执行顺序也是根据`<script>`书写位置决定的

6）延迟执行JS文件

`<script>`标签有一个布尔型属性defer，设置该属性能够将JS文件延迟到页面解析完毕再运行
defer适用于外部JS文件，不适用于script标签包含的脚本

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>延迟执行JS</title>
</head>
<body>
<script src="demo1.js" defer></script>
<script>
    alert("里边")
</script>
<p>今天天气真好我有点热</p>
</body>
</html>
```

#### 07）异步加载JS文件
在默认情况下，网页都是同步加载外部 JavaScript文件的，如果JavaScript文件比较大就会影响后面HTML代码的解析，所以就是可以最后加载Javascript文件。

现在可以为`<script>`标签设置 async属性，让浏览器异步加载 Javascript文件，即在加载 javaScript文件时，浏览器不会暂停，而是继续解析。这样能节省时间，提升响应速度。

async是HTML5新增的布尔型属性，通过设置asnc属性，就不用考虑< script标签的放置位置，用户可以根据习惯继续把很多大型 Javascript库文件放在`<head>`标签内。

### 02.基础调试代码
#### 01.alert()
JavaScript 语句是发给浏览器的命令。这些命令的作用是告诉浏览器要做的事情
alert() 语句让浏览器弹出一个窗口，窗口里的内容就是 alert() 中的内容
```js
    alert(125);
    alert("大帅比");
    var sex = "girl";
    alert(sex);
```

#### 02.console.log()
console.log可以打印出你想要看到的信息
<img src=https://upload-images.jianshu.io/upload_images/3532891-70178a0e27a56ce0.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240>
```js
    console.log("hello world");
```

### 03.document.write()方法
可以向HTML输出流中插入你传入的内容，浏览器会按着HTML元素依次顺序依次解析它们，并显示出来。

需要注意的是，如果在文档加载完成后（即HTML输出已完成），再使用document.write()方法来要求浏览器来解析你的内容，

则浏览器就会重写整个document，导致最后的这个document.write()方法输出的内容会覆盖之前所有的内容
```js
    document.write("哈哈");
    document.write("<a href='###'>点我上天</a>");
```

### 04.JS基本词法
#### 01）区分大小写
JavaScript严格区分大小写，为了避免输入混乱和语法错误，建议采用小写字符编写代码。在以下特殊情况下可以使用大写形式：
- 构造函数的首字母建议大写
- 如果标识符由多个单词组成，可以考虑使用骆驼命名法—除首个单词外，后面单词的首字母大写

#### 02）标识符

- 标识符指的是变量、函数、属性的名字，或者函数的参数。
- 标识符命名是有规范的
- 第一个字符必须是一个字母、下划线（_）或一个美元符号（$），其他字符可以是字母、下划线、美元符号或数字
- 不能含有空格 不能以关键字或保留字命名
>关键字：<img src=https://upload-images.jianshu.io/upload_images/3532891-3b6335d82bedadba.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240>
>保留字(保留字在这门语言中还没有任何特定的用途,但它们有可能在将来被用作关键字 ):<img src=https://upload-images.jianshu.io/upload_images/3532891-64126f8895687e52.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240>

#### 03）注释
注释就是不被解析的一串字符。 JavaScript注释有以下两种方法
- 单行注释：∥单行注释信息

- 多行注释：/*多行注释信息*/

#### 04）语句
- JS中的语句以一个分号 ; 结尾
- <img src=https://upload-images.jianshu.io/upload_images/3532891-719ec63ea214cbd4.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240>
- 虽然语句结尾的分号不是必需的,但我们建议任何时候都不要省略它。因为加上这个分号可以避免 很多错误 

#### 05）变量
- 变量相当于容器，值相当于容器内装的东西，而变量名就是容器上贴着的标签，通过标签可以找到变量，以便读、写它存储的值

- 为一块内存区域起的代号，通过这个代号，程序就可以把对应类型的数据保存到这个内存区域来完成相关计算的要求

- ECMAScript 的变量是松散类型（弱类型，动态类型）的,所谓松散类型就是可以用来保存任何类型的数据。换句话说, 每个变量仅仅是一个用于保存值的占位符而已

#### 06）变量的使用

- 语法: var 关键字  + 变量名称  = 数据 。等号右边的数据给等号左边变量名进行赋值

- 在一个var语句中，可以声明一个或多个变量，也可以为变量赋值，未赋值的变量初始化为 undefined(未定义)值。当声明多个变量时，应使用逗号运算符分隔

- 在 JavaScript中，可以重复声明同一个变量，也可以反复初始化变量的值
```js
    var name = "xiaowang";

    var sex = "女" , age = 18;
    var sex2 ;
    var sex3 , age2;
    var sex4 , age3 = 19;
    console.log(sex,age);


    var score = 100;
    score = 120;
    console.log(score);
    var score = 150;
    console.log(score);
```

#### 07）变量提升
- JavaScript在预编译期会先预处理声明的变量，但是变量的赋值操作发生在JavaScript执行期，而不是预编译期

- Javascript引擎的解析方式是：先解析代码，获取所有被声明的变量，然后再一行一行地运行这样，所有声明的变量都会被提升到代码的头部，这就叫作变量提升( Hoisting)。
```js
    /*
    * 1. 正常执行
    * */
    var a = 1;
    console.log(a);//1


    /*
    * 2. 没有声明和赋值 直接使用
    * */
    // console.log(b);//报错  b变量找不到 未声明


    /*
    * 3. 在使用后边声明
    * */
    console.log(c);//undefined  声明了但是找不到值
    var c;

    /*
    * 4. 在使用后边声明并赋值
    * */
    console.log(d);//undefined
    var d = 3;


    /*
    * 5.以下代码的真正的执行方式是？
    * */

    console.log(e);
    var e = 10;
    console.log(f);
    var f = 20;
    var g = 30;
    console.log(g);
    var h = 40;

    //答案：
    var e , f , g , h ;
    console.log(e);
    e = 10;
    console.log(f);
    f = 20;
    g = 30;
    console.log(g);
    h = 40;
```

#### 08）变量类型
JavaScript是弱类型语言,对于变量类型的规范比较松散。具体表现如下。

 - 变量的类型分类不严谨、不明确,带来使用的随意性。

 - 声明变量时,不要求指定类型。

 - 使用过程不严格,可以根据需要自动转换变量类型。

 - 变量的转换和类型检查没有一套统一、规范的方法,导致开发效率低下

#### 09) 变量污染
定义全局变量有3种方式：
- 在任何函数体外直接使用var语句声明。
- 直接添加属性到全局对象上。在Web浏览器中,全局作用域对象为 window
- 直接使用未经声明的变量,以这种方式定义的全局变量被称为隐式的全局变量。
全局变量在全局作用域内都是可见的,因此具有污染性。大量使用全局变量会降低程序的可靠性,用户应该避免使用全局变量

#### 10) 练习
两个变量的值互相交换
```JavaScript
//普通的做法就是声明多一个临时变量tmp，进行数据交换过程中的缓存。这样的做法直观，易懂。但是，会增加内存的使用。
    var a = 1,
        b = 2,
        tmp;
 
    tmp = a;
    a = b;
    b = tmp;

//算术运算,通过算术运算过程中的技巧，可以巧妙地将两个值进行互换。但是，有个缺点就是变量数据溢出。因为JavaScript能存储数字的精度范围是 -253 到 253。所以，加法运算，会存在溢出的问题。
    var a = 1,
        b = 2;
    
    a = a + b; // a = 3, b = 2
    b = a - b; // a = 3, b = 1
    a = a - b; // a = 2, b = 1

//其他方法可以以后学习～
```

## 三、JS数据类型
### 01.数据类型－声明变量练习：
```JavaScript
// 声明一个变量a，值为：3
// 声明一个变量b，值为：null
// 声明一个变量c，值为："Hello!"
// 声明一个变量d，值为：true
// 声明一个变量e，不赋值
// 声明一个变量f，值为""
    var a = 3;
    var b = null;
    var c = "hello";
    var d = true;
    var e ;
    var f = "";
    var g = [1,2,3,4];//数组
    var h = function(){};//函数
```
### 02.typeof 操作符 
- 我们需要有一种手段来检测给定变量的数据类型-typeof 就是负责提供这方面信息的操作符格式为 typeof（a）或 typeof a ；

- 有些时候 typeof 操作符会返回一些令人迷惑但技术上却正确的值
>把null归为Object类型，而不是作为特殊的值
把函数归为Function类型，而不是Object类型的一个子类
```js
    console.log(typeof a);//number
    console.log(typeof (b));//object
    console.log(typeof (c));//string
    console.log(typeof (d));//boolean
    console.log(typeof (e));//undefined
    console.log(typeof (f));//string
    console.log(typeof (g));//object
    console.log(typeof (h));//function  
```

### 03.数据类型分类
- JS数据类型分为两种：简单的值（原始值）和复杂的数据结构（泛指对象）。
- 值包含字符串、数字、布尔值。还有两个特殊的值 null（空值）和undefined（未定义）
- 对象包括狭义对象、数组和函数
	数据类型	     说明
	null	        空值、表示非对象
	undefined	    未定义的值,表示未赋值的初始化值
	nunber	        数字,数学运算的值
	string	        字符事,表示信息流
	boolean	        布尔值,逻辑运算的值
	object	        对象。表示复合结构的数据集

### 04.Undefined类型
#### 1）解释
- Undefined类型只有一个值，即undefined。在使用var声明变量但未对其加以初始化时，这个变量的值就是undefined。
- 我们不会对一个值设置undefined，一般都是出现错误的时候，才会被我们打印出来
#### 2）常见的Undefined环境
- 变量被声明了，但没有赋值时，就等于undefined
```js
    //打印a的时候，找到a了 但是找不到a的值，所以返回一个undefined
    var a;
    console.log(a);
    console.log(a+1);//undefined+1  计算不了

    //不声明b，直接使用b，js直接报错  ReferenceError： b is not defined
    //说明完全没有找到b这个变量 代码报错停止运行
    console.log(b)
```

- 调用函数时，应该提供的参数没有提供，该参数等于undefined
```js
    // 声明函数使用function关键字 函数没有调用是完全不执行的
    function add(a,b) {
        console.log(a)
        console.log(b)
        alert(a+b);
    }
    // 调用函数 函数名+（）  传入参数
    add(1,2);

    //再次调用函数（没有给够参数）
    add(1);*/

```

- 对象没有赋值的属性，该属性的值为undefined
```js
    // 创建一个对象
    var yourGirlFriend={
        name:"lily",
        age:18,
        length:180
    }
    // console.log(yourGirlFriend.name);
    console.log(yourGirlFriend.color);*/
```

- 函数没有返回值时，默认返回undefined
```js
    function reduce(a,b) {
        // 函数只要不写return 就没有返回值
        alert(a-b);
        // return a-b;//返回a-b
    }
    // 调用函数
    var num1=reduce(4,2);
    console.log(num1)

    console.log(reduce(4,1));
```
#### 3）检测一个变量是否初始化，如果没有，就为其赋值
```js
// a==undefined
// typeof a == 'undefined'
```

### 05.Null类型
#### 01）Null类型解释
- null 类型是第二个只有一个值的数据类型，这个特殊的值是 null。
- 从逻辑角度来看，null 值表示一个空对象指针，而这也正是使用 typeof 操作符检测null时会返回"object"的原因

#### 02）常见的 null 环境

- 作为函数的参数，表示该函数的参数不是对象
```js
        function fn(a,b) {
            alert(a+b);
        }
        // 需要传递参数，但是我们暂时不想传递，或者不需要传递，那么我们可以传一个空对象null
        fn(null,null)

        /*ajax有个方法send(),send方法参数是你要向服务器传递的值
        但是get方法是在地址栏拼接值，所以不需要send传递，所以我们在send中写一个参数null，告诉他我不想在这里传*/
```
- 作为对象原型链的终点
```js
//比如："123"--->String--->Object--->null
```

- 如果定义的变量准备在将来用于保存对象，那么最好将该变量初始化为null而不是其他值
```js
    var a = null;
    function fn1() {
        a=2;
    }
    fn1();
    console.log(a);
```

### 06 Undefined和Null
- Undefined派生自Null，两者都是表示空缺值，转换成布尔值都是假值，可以相等
- 但是Undefined和Null属于两种不同的类型
- Undefined隐含着意外的空值，而Null隐含着意料之中的空值。因此设置一个变量、参数为空的时候，建议使用null而不是undefined

### 07.Number类型
####01.解释
数字（Number）也称为数值或者数
- 整数，浮点数值（数字直接量）
- 八进制数（010、025）
- 十六进制数（0xa、0x1c）
- 二进制数
- 科学计数法
- Number.MIN_VALUE
- Number.Max_VALUE
- Infinity
- NaN
####02.整数，浮点数值（数字直接量）
当数字直接出现在程序中时候，被称为数字直接量
JS所有的数字都是以64位浮点数存储，所以2和2.0是同一个数字
```js
    var num1 = 19;//整数
    console.log(num1);

    var num2 = 18.11112;//浮点数
    console.log(num2);
```
#### 03.八进制数

```js
    var num3 = 010;//数字前加一个0 代表8进制数
    console.log(num3);
```
*八进制运算得到十进制*

#### 04.十六进制数

```js
    var num4 = 0xff;//数字前加上0x 代表十六进制数
    console.log(num4);
```
*十六进制运算得到十进制*

#### 05.二进制数(支持性不好，谨慎使用)

```js
    var num5 = 0b11;//数字前加上0b 代表二进制数
    console.log(num5);
```
#### 06.科学计数法

```js
    //用E代表底数10  后边跟E的指数 可以是正负值
    var num5 = 1.2E-7;
    console.log(num5);//1.2E-7
    console.log(num5+1);//1.00000012   运算以后 变成直接量显示
```
#### 07.最大值最小值

```js
// 在js中数字也是有最大值和最小值的支持的，如果超过最大值或最小值，就可能计算有误
    console.log(Number.MIN_VALUE);//支持数字的最小值
    console.log(Number.MAX_VALUE);//支持数字的最大值
```
#### 08.Infinity

```js
    // 分母为0会构成无穷大Infinity 或负无穷大-Infinity
    var num6 = 5/0;
    console.log(num6);//Infinity

    var num7 = -5/0;
    console.log(num7);//-Infinity

    console.log(typeof (Infinity));//无穷大和无穷小都是属于number类型

    // 关于Infinity的运算， 无法计算 加减乘除一个数字都是Infinity，Infinity和Infinity计算，加法乘法为Infinity，其他为NaN
    console.log(Infinity + 1);//Infinity
    console.log(Infinity - 1);//Infinity
    console.log(Infinity - 1000000000000000000000);//Infinity
    console.log(Infinity - Infinity);//NaN
    console.log(Infinity * Infinity);//Infinity
    console.log(Infinity + Infinity);//Infinity
    console.log(Infinity / Infinity);//NaN

    //Infinity和自身相等  其他比较正常
    console.log(Infinity > 1);//true
    console.log(Infinity < 1);//false
    console.log(Infinity == 1);//false
    console.log(Infinity > Infinity);//false
    console.log(Infinity == Infinity);//true
    console.log(Infinity < Infinity);//false
    console.log(Infinity > -Infinity);//true
```
#### 09.NaN

```js
    // NaN,即非数值(Not a Number)是一个特殊的数值,这个数值用于表示一个本来要返回数值的操作数未返回数值的情况(这样就不会抛出错误了)
    var num8 = "李沛华"-1;
    console.log(num8)//NaN

    // NaN特点：无论和谁比较都是fasle  无论和谁计算都是NaN
    console.log(NaN+1);//NaN
    console.log(NaN>1);//fasle
    console.log(NaN==1);//fasle
    console.log(NaN<1);//fasle

    //使用isNaN全局函数可以判断NaN
```
#### 10.isNaN方法的使用

- isNaN方法检测一个值是不是非纯数字 , 如果非纯数字就返回true  如果是纯数字就返回false

- 案例：点击检测的时候，判断是不是全部是数字

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>isNaN</title>
</head>
<body>
    请输入您的电话号码：
    <input id="ipt" type="text">
    <button id="btn">检测</button>
    <script>
        /*
        *   1、点击按钮 (给按钮绑定点击事件)
        *   2、获取input的值ss
        *   3、使用isNaN检测
        *   4、判断检测的值是true还是false
        *   5、如果是true则 输入的值不是纯数字 如果为false 则是纯数字
         */

        // 0、获取标签
        /*document(文档)
        . 成员访问  访问文档里的属性或方法
        get是获取
        Element是元素
        By是通过
        Id  id名  括号里不是变量 要加上引号*/
        // 得到值 需要用一个变量保存这个元素
        // 命名规则 凡是获取DOM的元素的变量名 同意o开头，后边第一个字母大写
        var oIpt = document.getElementById("ipt");
        var oBtn = document.getElementById("btn");

        // 1、当点击btn的时候  onclick是点击事件  后边把一个匿名函数赋值给oBtn.onclick
        // 这个时候，当点击btn的时候，函数就会执行
        oBtn.onclick=function () {
            //2 获取input的值  并用变量保存
            var userCon = oIpt.value;
            // 3、判断是否纯数字 isTrue为true 则包含其他字符  为false则纯数字
            var isTrue = isNaN(userCon);
            //4、判断并执行
            //     如果isTrue为true 则弹出请重新输入，否则弹出输入正确
            if (isTrue == true) {
                alert("请重新输入");
            }else{
                alert("输入正确");
            }
        }



        /*// 上边代码优化如下
        var oIpt = document.getElementById("ipt");
        var oBtn = document.getElementById("btn");
        oBtn.onclick=function () {
            if (isNaN(oIpt.value)) {
                alert("请重新输入");
            }else{
                alert("输入正确");
            }
        }*/
    </script>
</body>
</html>
```

#### 11.浮点数溢出
执行数值计算，要防止浮点数溢出，例如 0.1+0.2不等于0.3
因为js执行二进制浮点数算术标准而导致的问题。
解决方法：浮点数的证书运算是精确的，所以消暑表现的问题可以通过指定精度来避免。比如（1+2）/10

####  12.类型转换之Number方法
Number方法 将其他类型转换成number类型  Number方法会返回一个转换后的值

```js
    // 1、Number转  数字转数字  还是原来的值

    // 2、字符串转数字
    console.log(Number(""));//0 空字符串-->0
    console.log(Number("   "));//0 都是空格的字符串-->0
    console.log(Number("123"));//0 纯数字的字符串-->相对应的数字
    console.log(Number("1a23"));//0 非纯数字的字符串-->NaN


    //3、布尔值转数字
    console.log(Number(true));//1  true-->1
    console.log(Number(false));//0  false-->0

    // 4、undefined转数字
    console.log(Number(undefined));//NaN  undefined-->NaN

    // 5、null转数字
    console.log(Number(null));// 0   null--->0

    // 6、object(数组和对象)转数字
    console.log(Number([]));//0 空数组-->0
    console.log(Number([1,2,3]));//NaN 一般非空数组-->NaN
    console.log(Number([1]));//1 数字只有一个值，并且是数字-->当前数字
    console.log(Number(["1"]));//1 数字只有一个值，并且是数字值的字符串-->当前数字
    console.log(Number(["a"]));//0 数字只有一个值，并且是非数字-->NaN

    console.log(Number({}));//NaN  空对象-->NaN
    console.log(Number({name:"lily"}));//NaN  非空对象-->NaNz
```
#### 13.类型转换之parseInt()
parseInt是一个全局方法,它可以把值转换为整数

- 第1步,先解析位置0处的字符,如果不是有效数字,则直接返回 NaN。
- 第2步,如果位置0处的字符是数字,或者可以转换为有效数字,则继续解析位置1处的字符,如果不是有效数字,则直接返回位置0处的有效数字。
- 第3步,以此类推,按从左到右的顺序,逐个分析每个字符,直到发现非数字字符为止。
- 第4步,parseInt()将把前面分析合法的数字字符全部转换为数值并返回。

>注意：
浮点数中的点号对于parseInt来说属于非法字符,因此不会转换小数部分值。
如果是以0开头的数字字符串,则parseInt()不会把它作为八进制数字处理
如果是以0x 开头的数字字符串,则 parseInt()会把它作为十六进制数字处理:先把它转换为十六进
制数值,然后再转换为十进制的数字返回。

>parsInt也支持基模式，可以把不同进制的数字字符串转换为整数
```js
    console.log(parseInt(123));//123
    console.log(parseInt("a123"));//NaN
    console.log(parseInt("1a123"));//1
    console.log(parseInt("10a23"));//10
    console.log(parseInt("100px"));//100
    console.log(parseInt(12.3));//12
    console.log(parseInt("0xa"));//10

    console.log(parseInt(null));//NaN
    console.log(parseInt(true));//NaN


    /*
    * parseInt 支持基模式，把不同进制的数字字符串转换为整数
    * */
    var a = "abc123";
    console.log(parseInt(a,16));//11256099 把a当成16进制，转化为10进制输出
    var b = "111";
    console.log(parseInt(b,2));//7

    console.log(parseInt(5,3));//NaN  因为3进制没有5这个字符

    // 特殊情况如下：
    console.log(parseInt(1,1));//NaN
    console.log(parseInt(0,1));//NaN
    console.log(parseInt(0,0));//0
```
#### 13.类型转换之parseFloat()

>parseFloat()也是一个全局方法，它可以把值转换成浮点数，即它能够识别第一个出现的小数点，而第二个小数点视为非法。解析过程和parseInt相同。

>parseFloat()的参数必须是十进制的字符串，对十六进制和八进制前的0进行忽略或返回0。
```js
    console.log(parseFloat(123));//123
    console.log(parseFloat(12.3));//12.3
    console.log(parseFloat("12.3.3"));//12.3
    console.log(parseFloat("a12.1"));//NaN
```
####14.类型转换之乘号运算符
如果变量乘以1，则变量会被JS自动转换成数值，如果无法转换成合法数值，则返回NaN
```js
    /*
    *   如果说变量乘以1  变量就会被自动隐式转换为数字类型，如果转不了就变成NaN
    * */
    var a = "1";
    console.log(a * 1);//number类型的  1


    var b = "1a";
    console.log(b * 1);//NaN

    /*
    *   减法也可以
    * */
    var c = "1";
    console.log(c - 0);//number类型的  1


    var d = "1a";
    console.log(d - 0);//NaN

    /*除1也可以*/
    var e = "1";
    console.log(e / 1);//number类型的  1

    var f = "1a";
    console.log(f / 1);//NaN    
```

### 08.string类型
JavaScript字符串(String)就是由零个或多个Unicode字符组成的字符序列。零个字符表示空字符串。

####01.字符串直接量
- 子行串必须包含在单引号或双引号中
- 如果字符串包含在双引号中,则字符串内可以包含单引号;反之,也可以在单引号中包含双引号
- 在ECMAScript 3中,字符串必须在一行内表示,换行表示是不允许的，如果要换行显示字符串,可以在字符串中添加换行符(\n)
- 在ECMAScript 5中,字符串允许多行表示.实现方法:在换行结尾处添加反斜杠(\).反斜杠和换行符不作为字符串直接量的内容
- 在字符串中插入特殊字符,需要使用转义字符,如单引号,双引号等
- 字符串中每个字符都有固定的位置.第1个子符的下标位置为0,第2个字符的下标位置为1...···以此类推,最后一个字符的下标位置是字符串长度减1
```js
    var str1 = '093284yrc091708)(*&(^&(*&T';
    var str2 = "kajhx  askjh &*(";
    var str3 = `9287O&*b`;

    var str4 = "小王他妈妈说：'他要把翠花嫁给我'";
    console.log(str4);

    var str5 = "今天天气\n真好"
    console.log(str5);

    var str6 = "今天天气\
真好";
    console.log(str6);  
```
####02.转义字符
- 转义字符是字符的一种间接表示方式。在特殊语境中,无法直接使用字符自身
>比如：由于 JavaScript已经赋子了双引号为字符串直接量的标识符,如果在字符串中包含双引号,就必须
使用转义字符表示

- 一些字符加上反斜杠后会表示特殊字符,而不是原字符本身,这些特殊转义字符被称为转义序列
>\0     Null字符(\u0000)
\b      退格符(\u0008)
\t      水平制表符(lu0009)
\n      换行符(lu000A)
\v      垂直制表符(\u000B)
\f      换页符(\u000C)
\r      回车符(\u000D)

- 如果在一个正常字符前添加反斜杠,JavaScript会忽略该反斜杠
```js
    var str = "小明妈妈说:\"今天天气真好\"";
    console.log(str);

    var str2 = "小明妈妈说:\"\今\天\天\气\真\好\"";
    console.log(str2);

    var str3 = "看我斜杠：\\"
    console.log(str3);
```
####03.字符串操作
借助String类型的原型方法,可以灵活操作字符串（后面各章节中详细介绍）
- 在JavaScript中,可以使用加号(+)运算符连接两个字符串
- 使用字符串的length属性获取字符串的字符个数(长度）
- 在ES5中，字符串可以作为只读数组使用，可以通过中括号运算符添加下标访问某一个值。下标从0开始，最大位置的下标是length-1
```js
    var str = "老师说";
    var say = "你好啊";
    console.log(str+say);//老师说你好啊
    console.log(str + 1);//老师说1
    console.log(str + 1);//老师说1
    console.log(1 + 1);//2
    console.log("1" + 1);//11
    console.log(1 + "1");//11

    var str1 = "今天是个好天气123 b5";
    console.log(str1.length);//13

    console.log(str1[0]);//今
    //获取最后一个字符
    console.log(str1[str1.length-1]);//5
```

####04.字符串小练习
用户提交账号密码的时候，判断是否正确 已知账号是lipeihua  密码是1234561
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>字符串练习</title>
</head>
<body>
<!--
    用户提交账号密码的时候，判断是否正确 已知账号是lipeihua  密码是1234561
-->
请输入账号名：
<input type="text" id="user" autofocus>
请输入密码：
<input type="password" id="pass">
<button id="btn">登录</button>
<script>
    /*
    * 1.获取元素
    * 2.点击事件
    * 3.判断账号是否正确(点击以后可以直接获取账号密码)
    * 4.判断密码是否正确
    * 5.如果不正确 清空重新输入  正确则返回登陆成功
    * */
    var oUser = document.getElementById("user");
    var oPass = document.getElementById("pass");
    var oBtn = document.getElementById("btn");

    oBtn.onclick = function () {
        //用userUser 保存点击的时候，用户输入的用户名
        var userUser = oUser.value;
        //用userPass 保存点击的时候，用户输入的密码
        var userPass = oPass.value;

        // 判断
        if(userUser == "lipeihua"){
            if (userPass == 1234561) {
                alert("送你一个小发发");
            }else{
                alert("小伙子 你的密码不对哦")
                oPass.value = "";
                oPass.focus();
            }
        }else{
            alert("用户名错误");
            // userUser = "";//千万不要只改变变量 因为这个只是对变量重新赋值，没有操作value值
            oUser.value = "";

            // 让表单获取焦点
            oUser.focus();
        }

    }

</script>
</body>
</html>
```
####05.String方法
String方法是可以将其他类型转换成字符串类型
```js
    //1.null类型的转换
    console.log(String(null));//字符串的 'null'

    //2.undefined转换
    console.log(String(undefined));//字符串的'undefined'

    //3.number类型的转换
        //转换规则：普通数字直接变成字符串  其他进制先转换成10进制然后在转换成相应的字符串 无穷大无穷小NaN都直接变成字符串
    console.log(String(123));//'123'
    console.log(String(-123));//'-123'
    console.log(String(010));//'8'
    console.log(String(0xff));//'255'
    console.log(String(4E-5));//'0.00004'
    console.log(String(Infinity));//'Infinity'
    console.log(String(-Infinity));//'-Infinity'
    console.log(String(12.3));//'12.3'
    console.log(String(NaN));//'NaN'

    //4.布尔值的转换
    console.log(String(true));//'true'
    console.log(String(false));//'false'

    //5.对象的转换
    console.log(String([]));//空字符串 ''
    console.log(String([1]));//'1'
    console.log(String([1,2,3]));//'1,2,3'
    console.log(String({}));//[object object]
    console.log(String({name:"lily"}));//[object object]
```
#### 06.toString()方法

- 我们的代码中有+（加号）运算符等情况下，它在这种情况下（字符串 + 其它什么东西），会调用toString()方法，将其它类型的东西转化为字符串，再和原始字符串拼接成一个字符串

- 除了null和undefined之外，其他的类型(数值、布尔、字符串、对象)都有toString()方法，它返回相应值的字符串表现(并不修改原变量)。
- 每个对象都有一个toString()方法。
- 当该对象被表示为一个文本值时，或者一个对象以预期的字符串方式引用时自动调用。
```js
    (1).toString()      // "1"

    [1,2].toString()    // "1, 2"

    ({}).toString()     // [object Object]

    true.toString()     // "true"

    null.toString()     // Uncaught TypeError: Cannot read property 'toString' of null

    undefined.toString()  // Uncaught TypeError: Cannot read property 'toString' of null
```

### 09.Boolean类型
- 布尔类型仅包含两个固定的值：true和false。其中true代表真，false代表假。

  #### 01.类型转化之Boolean方法
```js
    //1、null
    console.log(Boolean(null));//false

    //2.undefined
    console.log(Boolean(undefined));//false

    //3.number
    //数字转布尔值   非0为true  0为false NaN为false
    console.log(Boolean(123));//true
    console.log(Boolean(-123));//true
    console.log(Boolean(0));//false
    console.log(Boolean(1.23));//true
    console.log(Boolean(NaN));//false
    console.log(Boolean(Infinity));//true
    console.log(Boolean(010));//true
    console.log(Boolean(0xa));//true


    //4.string

    //空为false  非空为true
    console.log(Boolean("123"));//true
    console.log(Boolean(""));//false
    console.log(Boolean("    "));//true


    //5.object
    //对象类型都转换成true
    console.log(Boolean([]));//true
    console.log(Boolean([1,2,3]));//true
    console.log(Boolean([0]));//true
    console.log(Boolean({}));//true
    console.log(Boolean({name:"lily"}));//true
```
####02.类型转化之双重逻辑非
一个逻辑非运算符（！）可以把值转换为布尔值并取反，两个就是转换成正确的布尔值

```js
console.log(!!0);   
```
####03.Boolea练习
点击按钮的时候，当input为空，则把input边框变红，否则是黑的
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Boolean类型</title>
    <style>
        #ipt{
            border:1px solid #000;
        }
    </style>
</head>
<body>
<input type="text" id="ipt">
<button id="btn">按钮</button>
<script>
    /*
    * 点击按钮的时候，当input为空，则把input边框变红，否则是黑的
    * */
    var oBtn = document.getElementById("btn");
    var oIpt = document.getElementById("ipt");
    oBtn.onclick = function () {
        var oIptValue = oIpt.value;
        //第一种判断 oIptValue == ""
        //第二种判断 oIptValue.length == 0
        //第三种判断 直接使用 if可以隐式转换的
        if(oIptValue){//oIptValue为非空
            oIpt.style.borderColor = "#000";
        }else{//oIptValue为空
            // 改变元素的行内样式
            oIpt.style.borderColor = "red";
        }
    }
</script>
</body>
</html>
```

## 四、运算符
运算符是根据特定的规则对操作数执行运算
JS共定义了47个运算符。
### 01.逗号操作符
- 逗号运算符是二元运算符,它能够先执行运算符左侧的操作数,然后再执行右侧的操作数,最后返回右侧操作数的值。
```js
    //逗号操作符执行计算总会返回最后一项
    var num4 = (4,5,6,7,8);
    console.log(num4);

    //i < 2,j < 4  前边为false 后边为true  这条语句仍然返回true  因为是逗号操作符总会返回后边的值
    for (var i = 0,j = 0; i < 2,j < 4; i++,j++) {
    	console.log(i+j);
    }

    //i < 2,j < 4  前边为true 后边为false  这条语句仍然返回false  因为是逗号操作符总会返回后边的值
    for (var i = 0,j = 0; i < 4,j < 2; i++,j++) {
        console.log(i+j);
    }
```
- 逗号运算符可以实现连续运算,如多个变量连续赋值
```js
    var a=1,b=2,c=3,d=4;
```

### 02.赋值操作符
- 赋值运算符左侧的操作数必须是变量,对象属性或数组元素,也称为左值
- 赋值运算有以下两种形式:
    1）简单的赋值运算(=):把等号右侧操作数的值直接赋值给左侧的操作数,因此左侧操作数的值会
发生变化。
    2）附加操作的赋值运算:赋值之前先对右侧操作数执行某种操作,然后把运算结果复制给左侧操作
数 比如 += -+ *= /= %=
```js
    //赋值运算符的结合性是从右向左,最右侧的赋值运算先执行,然后再向左赋值,以此类推,所以连续赋值运算不会引发异常
    var a = b = c = d = e = f =100;//连续赋值

    //常见错误：
    var c = 3;
    //等于判断  写成了一个等号，这个时候就一直为true  所以判断是否成立都会执行
    if (c = 4) {
        alert('hello');
    }
```

### 03.乘性操作符
- 乘性操作符分为  乘法  除法  求模（取余）
- 乘性操作符计算 会先把两个值 通过Number方法转换乘number类型  然后再计算
```js
    //乘法：
    console.log(3 * 3)//9
    console.log(-3 * 3)//-9
    console.log(-3 * -3)//9
    console.log(null * -3)//0
    console.log(undefined * -3)//NaN
    console.log(undefined * null)//NaN
    console.log(undefined * "123")//NaN
    console.log("10" * "123")//1230
    console.log("10" * 123)//1230
    console.log("abc" * 123)//NaN
    console.log(true * 123)//123
    console.log(true * false)//0
    console.log([] * false)//0
    console.log([] * [])//0
    console.log([] * {})//NaN
    console.log([] * {name:"lily"})//NaN
    console.log([2] * {name:"lily"})//NaN
    console.log([2] * {})//NaN
    console.log([2] * [3])//6
    console.log([2,3] * [3])//NaN
    console.log(Infinity * [3])//Infiity与任何相乘都是Infiity或-Infiity
    console.log(Infinity * Infinity)//Infinity
    console.log(Infinity * 0)//Infinity和0是NaN
    console.log(Infinity + Infinity)//Infinity
    console.log(Infinity - Infinity)//NaN


    //除法
    console.log(6 / 3);//2
    console.log(-6 / 3);//-2
    console.log(-6 / -3);//2
    console.log("abc" / 3);//NaN
    console.log(true / 3);//0.333333
    console.log(0 / 0);//NaN   0和0不能相除
    console.log(5 / 0);//Infinity
    console.log(Infinity / 0);//Infinity  被任意数除 都返回Infinity
    console.log(Infinity / Infinity);//NaN
    console.log([1] / Infinity);//0  当除数是Infinity的时候， 得到的结果是0
    console.log(8000000000000000 / Infinity);//0
    console.log([6] / 2);//3


    //取余（模运算） 取余的符号只看被除数（前边的）  不看除数
    console.log(5 % 3);//2
    console.log(-5 % 3);//-2
    console.log(-5 % -3);//-2
    console.log(5 % -3);//2
    console.log('abc' % -3);//NaN
    console.log('5' % -3);//2
    console.log('5' % Infinity);//-5
    console.log(Infinity % -3);//NaN
    console.log([5] % -3);//2
    console.log({} % -3);//NaN

```
### 03.减法操作符
有一个不能转化成数字就返回NaN，Infinity与任意数相减都是Infinity
技巧：
    使用值减去0 可以快速的把值转换成数字
```js
    console.log(5 - 2);//3
    console.log("5" - 2);//3
    console.log("a" - 2);//NaN
    console.log([] - 2);//-2
    console.log([5] - 2);//3
    console.log([5,4] - 2);//NaN
    console.log({} - 2);//NaN
    console.log(true - 2);//-1
    console.log(null - 2);//-2
    console.log(undefined - 2);//NaN
```
### 04.加法操作符
#### 01.概念
加法操作符除了运算以外，还有字符串拼接的功能
```js
    console.log(1 + 1);//2

    //加法运算中，如果出现一个是字符串  那么就把另一个转换成字符串
    //两个字符串相加，是将两个字符串链接再一起生成一个新的字符串
    console.log("1" + 1);//'11'
    console.log("abc" + 1);//'abc1'
    console.log("abc" + "abc");//'abcabc'
    console.log(null + "abc");//'nullabc'
    console.log(undefined + "abc");//'undefinedabc'
    console.log([] + "abc");//'abc'

    //空数组和对象拼接，都会把他们转换成字符串
    console.log([] + {});//'[object object]'
    //数组相加也是拼接字符串
    console.log([] + []);//''

    //两个对象拼接 也是转换成字符串
    console.log({} + {});//[obejct object][object object]


    console.log(undefined + null);//NaN
    console.log(true + true);//2
```
#### 02.加法操作符练习
```js
    var num1 = 1 + 2 + "a" + "b";//3ab
    var num2 = "a" + 1 + 2 + "b";//a12b
    var num3 = 1 + 2 + 3 + "a";//6a
    var num4 = "a" + 2 + 3 + 4;//a234

    var num5 = 1;
    var num6 = 2;
    alert("num5 + num6 = "+ num5 + num6);//'num5 + num6 = 12'


    var name = "李沛华";
    alert("我的名字是" + name);
```
#### 03.加法操作符使用2
让用户输入两个值 计算两个值的和,当点击按钮时  让box的宽度和高度发生变化 值为两个值的和
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>加法操作符使用</title>
    <style>
        #box{
            width: 100px;
            height: 100px;
            background-color: red;
        }
    </style>
</head>
<body>
    请输入第一个值<input type="text" id="ipt1">
    请输入第二个值<input type="text" id="ipt2">
    <button id="btn">你点我呀</button>
    <div id="box">

    </div>

    <script>
        var oBox = document.getElementById("box");
        var oBtn = document.getElementById("btn");
        var oIpt1 = document.getElementById("ipt1");
        var oIpt2 = document.getElementById("ipt2");

        oBtn.onclick=function () {
            //1.点击按钮的时候  先获取两个输入框的值，并计算一个和
            //2.获取输入框的值是字符串，要传换成数字再进行加法运算求和
            var iptAdd = Number(oIpt1.value) + Number(oIpt2.value);
            console.log(iptAdd);

            //3.将得到的和赋值给box的宽和高
            // 对元素的style属性中的width属性进行赋值 宽和高都是有单位的 单位是px
            //这样的方法 设置的样式 都是行内样式
            oBox.style.width = iptAdd + "px";
            oBox.style.height = iptAdd + "px";
        }
    </script>
</body>
</html>
```
#### 04.加法操作符练习3
每次点击按钮的时候，让con的内容的数值 每次加2
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>+=练习</title>
</head>
<body>
<div>
    <button id="btn">点击</button>
    <p id="con">0</p>

    <script>
        /*
         * 每次点击按钮的时候，让con的内容的数值 每次加2
         *
         * 1、获取元素
         * 2、点击事件
         * 3、获取con的值  innerHTML
         * 4、让con的值加2
         * 5、把con的值再给到con里 innerHTML
         */

        var oBtn = document.getElementById("btn");
        var oCon = document.getElementById("con");

        //2.绑定事件
        oBtn.onclick=function () {
            //3.获取con的值  获取元素的值 同样也是字符串  所以要转换成number
            var conCon = Number(oCon.innerHTML);
            //4.让con+2
            conCon += 2;
            //5.把计算好的值赋值到con中
            oCon.innerHTML = conCon;
        }
    </script>
</div>
</body>
</html>
```
#### 05.学生信息录入系统
每次可以再输入框输入名字  然后点击以后 名字可以累加在p标签中  并且每个名字换行显示
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>+=练习</title>
</head>
<body>
<div>
    <h2>学生信息录入系统</h2>
    <input type="text" id="ipt">
    <button id="btn">点击</button>
    <p id="con">李沛华</p>

    <script>
        /*
         * 每次可以再输入框输入名字  然后点击以后 名字可以累加在p标签中  并且每个名字换行显示
         *
         * 1、获取元素
         * 2、点击事件
         * 3、获取ipt的值
         * 4、把ipt的值再给到con里
         */

        var oBtn = document.getElementById("btn");
        var oCon = document.getElementById("con");
        var oIpt = document.getElementById("ipt");

        //2.绑定事件
        oBtn.onclick=function () {
            //3.获取ipt的值
            var iptCon = oIpt.value;
            //4.把ipt的值累加到con中
            //获取con原来的值 拼接上iptcon（新的值）  然后赋值给con.innerHTML(con的内容)
            //我们可以在拼接赋值的时候 把标签当成字符串拼接进去   innerHTML是可以解析标签
            //oCon.innerHTML = oCon.innerHTML + "<br>" + iptCon;
            oCon.innerHTML += "<br>" + iptCon;
        }
    </script>
</div>
</body>
</html>
```
### 05.递增递减操作符
- 递增(++)和递减(--)运算就是通过不断地加1或减1,然后把结果赋值给左侧，以实现改变自身结果的一种简洁方法

- 作为一元运算符,递增运算符和递减运算符只能作用于变量、数组元素或对象属性,不能作用于直
接量

- 递增和递减在运算之前都会试图转换值为数值类型,如果失败则返回 NaN。

- 根据位置不同,可以分为4种运算方式
>前置递增(++n):先递增,再赋值
前置递减(--n):先递减,再赋值
后置递增(n++):先赋值,再递增
后置递减(n--):先赋值,再递减 zz jz j rz j r d
```js
    // 无论是  ++a  还是 a++  都是让 a每次加1，如果两个代码都是独立运行，那么两个代码没有区别

    /*var a = 1;
    // 让 a 加一
    //a = a + 1;
    //a += 1;

    a ++;//a++是让a  每次加1
    a ++;//a++是让a  每次加1
    a ++;//a++是让a  每次加1
    console.log(a);*/


    /*var b = 1;
    ++ b;//让b每次加1
    ++ b;//让b每次加1
    ++ b;//让b每次加1
    ++ b;//让b每次加1
    console.log(b);*/


    // c++不是单独运行的时候，也就是有赋值操作的时候，那么是先执行赋值，然后再去加1
    // c++ 就是先赋值 后加1
    /*var c = 2;
    var d = c ++;
    console.log(c);//3
    console.log(d);//2*/


    // ++c  先加一 后赋值
    /*var c = 2;
    var d = ++ c;
    console.log(c);//3
    console.log(d);//3*/


    var a = 1;
    b = a++ + (a++) + 1 + (++a) + (a++) + (++a) + a + (++a);
    // b = 1 + 2 + 1 + 4 + 4 + 6 + 6 + 7;
    console.log(a);//7
    console.log(b);//17 31
```
### 06.关系运算
关系运算也称比较运算,需要两个操作数,运算返回值总是布尔值
#### 01.大小比较
- 比较大小关系的运算符有4个
>\>:如果第一个操作数小于第二个操作数,则返回true;否则返回 false
<=:如果第一个操作数小于或者等于第二个操作数,则返回 true;否则返回 false
\>=:如果第一个操作数大于或等于第二个操作数,则返回true;否则返回 false
\>:如果第一个操作数大于第二个操作数,则返回true;否则返回 false

- 比较运算中的操作数可以是任意类型的值,但是在执行运算时,会被转换为数字或字符串,然后再
进行比较。如果是数字,则比较大小; 如果是字符串,则根据字符编码表中的编号值,从左到右逐个比
较每个字符
> 1)如果两个操作数都是数字,或者一个是数值,另一个可以被转换成数字,则将根据数字大小进行比较
> 2)如果两个操作数都是字符串,则执行字符串比较。
> 3)如果一个操作数为NaN,或者被转换为NaN,则始终返回 false。
> 4)如果一个操作数是对象,则先使用 valueOf取其值,再进行比较:如果没有valueOf方法,则
使用toString取其字符串表示,再进行比较
> 5)如果一个操作数是布尔值,则先转换为数值,再进行比较。
> 6) 如果操作数都无法转换为数字或字符串,则比较结果为false
```js
    var num1 = 3;
    var num2 = 4;
    console.log(num1 < num2);//true
    console.log(num1 <= num2);//true
    console.log(num1 >= num2);//false
    console.log(num1 > num2);//false


    //数字和字符串相比  按照数字来比较
    console.log(1 < 4);//true
    console.log(1 < '4');//true
    console.log(1 < 'a');//false  1 和 NaN在比较

    //字符串和字符串比较 是按照每一位来比较的  先比较第一位 然后如果相等再比较第二位 等等等。。。
    //字符串比较的是ascII码的大小  数字<大写字母<小写ß字母
    console.log("14" < '4');//true
    console.log("abc" < '4');//false
    console.log("abc" < 'ab');//false

    //null和字符串比 是按照数字相比的  null转换成了数字
    console.log(null > 'abcd');//false
    console.log(undefined < 1);//false
    console.log(undefined < "abc");//false
    console.log(undefined < null);//false

    //两个{}相比 按照数字来比较  都是NaN  返回false
    console.log({} > {});//fasle

    //数组和对象比较  转换成了字符串比较  ""<'[obejct object]'
    console.log([] < {});//true

    //有数组没有数字  按照字符串比较
    console.log([4] > [14]);//true


    //布尔值和其他比较 都转换成数字比较
    console.log(true > -3);//true
    console.log(true > []);//true

    //布尔值和对象比较 也是按照数字比较的，对象转换成了NaN
    console.log(true == {});//fasle
```
#### 02.相等和全等
- 等值检测运算符包括4个：
>1)\==:比较两个操作数的值是否相等
2)!=:比较两个操作数的值是否不相等
3)===:比较两个操作数的值是否相等,同时检测它们的类型是否相同
4)!==比较两个操作数的值是否不相等,同时检测它们的类型是否不相同

- 在相等运算中,应注意以下几个问题"
>1)如果操作数是布尔值,则先转换为数值,其中false转为0,true转换为1.
2)如果一个操作数是字符串,另一个操作数是数字,则先尝试把字符串转换为数字。 
3)如果一个操作数是字符串,另一个操作数是对象,则先尝试把对象转换为字符串。
4)如果一个操作数是数字,另一个操作数是对象,则先尝试把对象转换为数字。
5)如果两个操作数都是对象,则比较引用地址。 如果引用地址相同,则相等; 否则不等。
6)NaN和任何值都不相等，包括自身
7)null和undefined值相等，但是是不同的数据类型

- 在全等运算中,应注意以下几个问题.
>1）如果两个操作数都是简单的值.,则只要值相等,类型相同,就全等.
2)如果一个操作数是简单的值.另一个操作数是复合型对象,则不全等。
3）如果两个操作数都是复合型对象,则比较引用地址是香相同.

### 07.逻辑运算
逻辑运算又称布尔代数，也就是布尔值的算术运算。
逻辑运算符包含：逻辑与（&&）、逻辑或（||）、逻辑非（！）
#### 01.逻辑与运算
逻辑与运算是只有两个数都是true的时候，才会返回true（一假即假）
>第一步：计算第一个操作数
第二步：如果第一个操作数转换成false，那么就会结束运算，直接第一个操作数
第三步：如果第一个操作数返回true，则计算第二个操作数的值
第四步：第二个操作数如果返回true  则逻辑与返回第二个操作数，否则返回第一个操作数
```js
    //假设用户输入的长度 在10 到20 之间  那么就成功
    var userLen = 15;
    //参照操作符优先级  比较操作符 大于 逻辑操作符
    console.log(userLen > 10 && userLen < 20);
```
#### 02.逻辑或运算
逻辑或运算（||），如果两个操作数都是true，或者其中一个是true的时候，会返回true。
>第一步：计算第一个操作数的值。
第二步：检测第一个操作数的值。如果左侧的表达式的值可以转换为true，那么就会结束运算。直接返回第一个操作数的值
第三步：如果第一个操作数可以转换为false，则计算第二个操作数的值。并返回第二个操作数的值
```js
    //小明的女朋友 有3个 或 5个是合法的  是其他的就不行
    var mingGrilFri = 4;
    console.log(mingGrilFri == 3 || mingGrilFri == 5);
```
#### 03.逻辑非运算
逻辑非运算，作为一元运算符，直接放在操作数之前，把操作数的值转为布尔值，然后取反返回
```js
    //如果说用户输入的全部都是数字  则返回成功
    // isNaN  判断传入的值 是否是纯数字  如果是纯数字则返回false  否则是true
    var userNum = '15701665563';
    if (isNaN(userNum)) {

    }else{
        alert("成功")
    }


    //优化
    if (!isNaN(userNum)) {
        alert("成功");
    }
```
**逻辑与和逻辑或的返回值不必是布尔值，但是逻辑非运算的返回值一定是布尔值**
#### 04.与或非练习
判断两个数，如果有一个是非数字，那么就提示用户，否则就计算两个数字的和
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>与或非练习</title>
</head>
<body>
<script>
    // 判断两个数，如果有一个是非数字，那么就提示用户，否则就计算两个数字的和
    var num1 = "3333";//input中拿到的值，只能是字符串
    var num2 = "4444";

    /*if (isNaN(num1) || isNaN(num2)){
        alert("两个数字中存在非数字")
    } else{
        alert(Number(num1) + Number(num2));
    }*/


    if (!isNaN(num1) && !isNaN(num2)){
        alert(Number(num1) + Number(num2));
    } else{
        alert("两个数字中存在非数字")
    }
</script>
</body>
</html>
```
### 08.短路原理
- && || 遵循“短路”原理
- 若&&中第一个表达式为 fasle 则不会处理下一个表达式；||第一个表达式为true则不会执行下一个
- 当 || 时，找到为 true 的分项就停止处理，并返回该分项的值；否则执行完，并返回最后分项的值。
- 当&&时，找到为false的分项就停止处理，并返回该分项的值
```js
    // 这种类似的题目，一般不考虑整体返回值，而是看前一句条件是否满足，然后看后一句代码是否执行
    var a = 2; var b = 3;
    (a < b)&&(a = 5);
    console.log(a);//5

    var a = 6; var b = 3;
    (a < b)&&(a = 5);
    console.log(a);//6


    var a = 2; var b = 3;
    (a < b)||(a = 5);
    console.log(a);//2

    var a = 6; var b = 3;
    (a < b)||(a = 5);
    console.log(a);//5
```
### 09.一元运算
```js
    var a = "5";
    var b = 6;
    console.log(Number(a));

    console.log(typeof +a);//number

    // 一元加法运算对数字没有影响  但是对其他类型却转换成了数字
    console.log(+b);//6
    console.log(+a + 2);//7
    console.log(+"abc");//NaN
    console.log(+[]);//0
    console.log(+null);//0
    console.log(+undefined);//NaN
    console.log(+{});//NaN
    console.log(+false);//0

    // 一元减法 对数字没有加一个负数  对其他类型先转换成数字 然后添加一个负号
    console.log(-a + 2);//-3

    // if判断会自动把判断式转换成布尔值
    var a = 0;
    if(a){
        alert("成功")
    }else{
        alert("失败")
    }
```
### 10.字符串转数字总结
```js
var a = "4";
    // 第一种  Number方法
    console.log(Number(a));//4

    //第二种  一元运算
    console.log(+a);//4

    // 第三种 减0
    console.log(a - 0);//4

    // 第四种 parseInt 和 parseFloat
    //parseInt对字符串检测，从第一位开始检测，直到检测到非数字为止，然后将检测到的数字取整
    console.log(parseInt("100px"));;//100
    console.log(parseInt("10abc10"));;//10
    console.log(parseInt("abc10"));;//NaN
    console.log(parseInt("10.533abc10"));;//10
    console.log(parseInt("10.a001bc10"));;//10

    //parseFloat对字符串检测，从第一位开始检测，直到检测到非数字为止 保留小数
    console.log(parseFloat("100px"));;//100
    console.log(parseFloat("10abc10"));;//10
    console.log(parseFloat("abc10"));;//NaN
    console.log(parseFloat("10.533abc10"));;//10.533
    console.log(parseFloat("10.a001bc10"));;//10




    // 效果：点击获取元素宽度  并每次加10
    //1 获取元素的宽度（这种方法只能获取元素的行内样式）
    var oBox = document.getElementById("box");
    var oBtn = document.getElementById("btn");
    var boxWidth = oBox.style.width;
    console.log(boxWidth);//'100px'
    // 2.对 btn 绑定点击事件
    oBtn.onclick = function () {
        //3.让宽度的值每次加10
        boxWidth = parseInt(boxWidth)+10+"px";
        //4.赋值
        oBox.style.width = boxWidth;
    }
```
### 11.三元运算符（三目运算符、条件运算符）
语法格式：b？x ：y
>b操作数必须是一个布尔型的表达式，x和y是任意类型的值
如果操作数b的返回值是true，则执行x的操作数，并返回该表达式的值
如果操作数b的返回值是false，则执行y的操作数，并返回该表达式的值
```js
    var num = true ? 3 : 2;
    console.log(num);

    // 定义变量a，然后检测a是否被赋值，如果被赋值，则使用该值，否则设置一个默认值
    var a;
    typeof a !="undefined"?a = a:a = 0;
    console.log(a);

    // 如果a大于b  则弹出你好  否则 弹出滚蛋
    // 方法1
    if (a > b){
        alert("你好");
    } else{
        alert("滚蛋");
    }

    // 方法2 三元运算
    a > b ? alert("你好"):alert("滚蛋");

    // 方法3 短路原理
    a > b || alert("滚蛋");
    a > b && alert("你好");

    //方法4:
    a > b && alert("你好")|| alert("滚蛋");
```
### 12.括号的作用
```js
    // 小括号的作用
        //1、提升优先级
        //2、函数调用
    
    // 中括号的作用：
        // 1、定义数组
        // 2、使用下标

    // 大括号的作用：
        // 1、定义对象
        // 2、书写代码块  大括号后可以不添加分号
    
    {
        var a = 10;
        var b = 20;
        console.log(a + b);
    }

```
### 13.操作符优先级
<img src=https://upload-images.jianshu.io/upload_images/3532891-1aa28642cbcbec32.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240>

### 14.综合练习
变量 year 中存放的是年份值，判断变量是不是闰年，var year;
```js
//年份能够被4整除且不能被100整除，或者年份能够被400整除
    var year = 2016;
    if (year % 4 == 0 && year % 100 != 0 || year % 400 ==0) {
        alert("是闰年")
    }
```

## 五、语句

### 01.什么是语句
- ECMA-262 规定了一组流程控制语句。语句定义了 ECMAScript 中的主要语法,语句通常由一个或者多个关键字来完成给定的任务。诸如:判断、循环、退出等。 

- 语句主要分为：声明、分支控制、循环控制、流程控制、异常处理等。、

### 02.声明语句
声明语句包含三种：声明变量、声明函数和声明标签
```js
    // 声明函数 使用function关键字
    function f() {

    }

    // 声明变量
    var a = 1;//有声明提升  作用域按照函数计算
    let b = 2;//无声明提升  作用域按照代码块计算
    const MAX = 100;//无声明提升  常量  不能被修改或者重新赋值

    // 声明Label:
    // 声明语句一般都是配合continue和break来使用的，在后边流程控制语句中讲解
    for1:
    for (var i = 0;i<3;i++){

    }
```
### 03.调试语句
debugger语句用于停止JS
debugger语句可以放在代码的任何位置用以脚本中止执行，但是不会关闭任何文件或者删除变量，类似在代码中设置断点
```js
    for (var i = 0; i < 5; i++) {
        debugger;
        console.log(1);
    }
```
### 04.if语句
#### 01.单分支if
- if (判断式){代码块}
- 如果判断式为真，则执行代码块。
- 判断式不一定要书写各种操作符，无论传递什么进去，if都会把它转换成布尔值 然后执行if代码
- 一般有 （ 当。。。。的时候  否则。。。。的时候   ）使用if语句
- if判断语句的代码块是单句，我们可以省略大括号(但是js中不建议这样书写)
<img src=https://upload-images.jianshu.io/upload_images/3532891-63dfc413936d1fa1.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240>
```js
    //【单分支if】声明变量 a、b，且赋值 a 和 b 都等于5；当 a 等于 b 时，重新对 b 赋值为10，并弹出 b 的新值
    var a = 5 , b = 5 ;
    // 如果a不等于b  那么整个if就不会执行  因为没有else
    // js是允许只书写if  不书写else 的
    /*if ( a == b ){
        b = 10;
        alert(b);
    }*/
```

#### 02.双分支 else语句
- else语句仅在if或者else/if语句的条件表达式为假的时候执行。
- if（判断式）{代码块1}else{代码块2}
- 如果判断式为真，则执行语句1，否则将执行语句2
<img src=https://upload-images.jianshu.io/upload_images/3532891-1f840e7f646ec214.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240>

```js
    //【双分支】声明变量 a赋值为100；当 a 大于 50 时，弹出“a真大”，否则弹出“a真小”
    var a = 100;
    if (a > 50){
        alert("a真大");
    }else{
        alert("a真小");
    }

    //【双分支】y值和x值相关。X大于等于3时，y值为2。X小于3时，y值为1
    var y = 4,x = 2;
    if (x >= 3){
        y = 2;
    }else{
        y = 1;
    }

    //【双分支】如果x大于y成立，则x值为y值加1，否则x值为y值减1
    var x = 3,y = 4;
    if (x > y){
        x = y + 1;
    }else{
        x = y - 1;
    }

    //【双分支】如果x大于y或者x小于z成立，则x值为z值，否则x值为y值
    var x = 1,y = 2,z = 3;
    if (x > y || x < z) {
        x = z;
    }else{
        x = y;
    }
```
#### 03.else if语句
- else if语句 可以构成多分支
- if (条件表达式) {语句1;} else if (条件表达式) {语句2;} ... else {语句3;} 
<img src=https://upload-images.jianshu.io/upload_images/3532891-0abb8983a12df5e4.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240>

```js
    // 【多分支】如果x值为3，y值为2，如果x值大于3，y值为1，如果x值小于3，y值为4
    var x = 3,y = 4;
    if (x == 3){
        y = 2;
    }else{
        // x不等3的情况 进入else
        if (x >3){
            y = 1;
        } else{
            y = 4;
        }
    }
    //else if()是在上一次判断的基础上 在剩下的条件中继续判断
    if (x == 3){
        y = 2;
    }else if (x > 3){
        y = 1;
    }else{
        y = 4;
    }

    //【多分支】x值为2，y值为1，如果x值比2小，y值为0，如果x值比10大，y值为10，如果x值小于4且大于3，y值为5，其他情况y为3
    var x = 2, y = 1;
    if (x < 2){
        y = 0;
    }else if (x >10){
        y = 10;
    }else if(x < 4 && x > 3){
        y = 5;
    }else{
        y = 3;
    }
```
#### 04.if语句的练习
用户输入成绩  然后弹出成绩的等级
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>if语句的练习</title>
</head>
<body>
请输入成绩（数字）：
<input type="text" id="ipt">
<p>等级：<span id="con"></span></p>
<script>
    /*
     * 用户输入成绩  然后弹出成绩的等级
     * 成绩是 >=90  A    >=80 <90  B  >=70 <80  C  >=60 <70  D     其他  Z
     */
    var oIpt = document.getElementById("ipt");
    var oCon = document.getElementById("con");
    oIpt.onchange = function () {
        // 获取表单的值，并转换成数值
        var userScroe = parseInt(this.value);
        if (userScroe >= 90){
            oCon.innerHTML = "A";
        }else if(userScroe >= 80){
            oCon.innerHTML = "B";
        }else if(userScroe >= 70){
            oCon.innerHTML = "C";
        }else if(userScroe >= 60){
            oCon.innerHTML = "D";
        }else{
            oCon.innerHTML = "Z";
        }
    }
</script>
</body>
</html>
```
### 05.switch语句
- switch语句专门用来设计多分枝条件结构。与else/if多分支结构相比，switch结构更加简介，执行效率更高。
- 语法如下：
>switch（表达式）｛
   case value1：语句1；break;
   case value2：语句2；break;
   …………
   default：语句
}
- switch语句根据表达式的支，一次与case后的表达式的value值进行比较。如果相等，则执行其后的语句段，只遇到break，或者switch语句结束才中止，如果不想等，则继续查找下一个case。
- switch语句包含了一个可选的default语句(switch的异常处理)，如果前边的case没有找到相等的条件，则执行default语句，它与else语句类似。
- switch语句是使用全等（===）来检测两个只的相等与否。所以会有一个值类型的比较
- case后可以是一个空语句，把多个条件放在一起检测
- 在switch语句中，case子句只是指明了执行的起点，但是没有指明终点，如果case后没有break语句，就会发生连续执行的情况，而忽略后边case的条件限制。
```js
var a = 6;
    switch (a) {
        case 1:
            alert(1);
            // break;
        case 2:
            alert(2);
            // break;
        case 3:
            alert(3);
            // break;
        case 4:
            alert(4);
            break;
        case 5:
        case 6:
        case 7:
            alert(8);
            break;
        default:
            alert(10)
    }
```

- 练习
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>switch练习</title>
</head>
<body>
请输入成绩（数字）：
<input type="text" id="ipt">
<p>等级：<span id="con"></span></p>
<script>
    /*
     * 用户输入成绩  然后弹出成绩的等级
     * 成绩是   100-->S    >=90  A    >=80 <90  B  >=70 <80  C  >=60 <70  D     其他  Z
     */
    var oIpt = document.getElementById("ipt");
    var oCon = document.getElementById("con");
    oIpt.onchange = function(){
        //获取用户输入的成绩
        var userScore = this.value;
        // 因为switchdo都是相等判断 所有我们都取 分数的第一位 然后判断相等 比如所有的90分以上  都是9开头

        userScore = parseInt(userScore / 10);
        switch (userScore) {
            case 10:
                oCon.innerHTML = "S";
                break;
            case 9:
                oCon.innerHTML = "A";
                break;
            case 8:
                oCon.innerHTML = "B";
                break;
            case 7:
                oCon.innerHTML = "C";
                break;
            case 6:
                oCon.innerHTML = "D";
                break;
            default:
                oCon.innerHTML = "D";
        }
    }
</script>
</body>
</html>
```

### 06.循环语句
在程序开发中，存在大量的重复性操作或计算，这些任务必须依靠循环结构来完成。
JS提供了 while for  do/while三种类型的循环语句
#### 01.while语句
while语句是最基本的循环结构。语法格式如下：

>while(判断式){
    语句
}
>当判断式为真的时候，执行语句。执行结束之后再次进行判断，直到判断式子为假，才跳出循环。
<img src=https://upload-images.jianshu.io/upload_images/3532891-22614d137344648b.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240>

```js
    // 用while()循环来计算1+2+3 ... +98+99+100的值。

    var i = 1;
    var num = 0;
    while(i <= 100){
        num += i;
        i ++;
    }
    console.log(num);

    // 也可以在循环语句中添加增量
    var i = 1;
    var num = 0;
    while(i++ <= 100){
        num += i;
    }

    //每次执行时，要让条件发生变化，否则将进入死循环
    var a = 4;
    while(a < 7){
        console.log(a);
        a ++ ;
    }

    // 将1-100之间  3的倍数找出来 并打印
    var i = 1;
    while(i <= 100){
        if (i % 3 == 0){
            console.log(i);
        }
        i++;
    }

```
#### 02.do/while语句
do/while与while循环非常相似，区别在与表达式的值是每次循环结束后去检查，而不是开始去检查。
因次do/while循环能够保证至少执行一次循环。而while就不一定了。
语法如下：
>do{
    语句
}while(判断式子)
<img src=https://upload-images.jianshu.io/upload_images/3532891-20cf3b7dad2e6171.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240>

```js
    var a = 3;
    do{
        console.log("hello");
    }while(a < 1);


    // 用do－while()循环来计算1+2+3 ... +98+99+100的值：
    var i = 1;
    var num = 0;
    do{
        num += i;
        i ++;
    }while(i <= 100);
    console.log(num)
```
#### 03.练习-计算年利率
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>计算年利率</title>
</head>
<body>
<input type="text" id="ipt">
<script>
    /*
    * 用户输入一个钱数  年利率为1.05(去年的利息和本钱 是下一年的本金)  翻倍需要几年
     */

    var oIpt = document.getElementById("ipt");
    var scale = 1.05;
    oIpt.onchange = function () {
        var userMoney = parseFloat(this.value);
        var fatalMoney = 2 * userMoney;
        var years = 0;

        //当用户的钱只要小于翻倍的钱，那么就让循环一直执行
        while(userMoney <= fatalMoney){
            // 循环体中，让本金每次执行都翻1.05倍，每一年循环一次
            userMoney *= scale;
            //每执行一次循环  让年数加1
            years ++;
        }
        alert("您的钱翻倍需要"+years+"年");

    }
</script>
</body>
</html>
```
#### 04.练习-判断登录
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>04.判断登录</title>
</head>
<body>
<script>
    /*
     * 接受 用户输入的账号和密码  只要账号不是laowang  密码不是 888888 我们就一直提示请重新输入  否则 提出输入成功
     */
    // prompt是包含输入框  确认和取消的弹窗 用户输入的值就是这个prompt方法的返回值  如果用户没有输入或输入空  则返回null
    //prompt第一个参数 是提示用户的话

    /*//1、页面刚进入 先弹窗让用户输入账号名和密码
    var userName = prompt("请输入用户名");
    var passWord = prompt("请输入密码");
    //2、如果判断不正确 就一直让弹出输入账号名密码  所以可以考虑while循环
    while(userName != "laowang" || passWord != "88888"){
        // 3、密码输入错 或者  账号输入错误  就进入while执行 弹窗
        userName = prompt("请输入用户名");
        passWord = prompt("请输入密码");
    }
    alert("欢迎光临  老王")*/




    /*// 方法二： 递归调用

    var userName = prompt("请输入用户名");
    var passWord = prompt("请输入密码");
    //因为每次输入完都要判断  所以需要封装一个 函数
    function isLogin() {
        if (userName != "laowang" || passWord != "88888"){
            userName = prompt("请输入用户名");
            passWord = prompt("请输入密码");
            isLogin();//递归算法（在函数中调用自身）
        }else{
            alert("欢迎光临 老王 你是老王吧")
        }
    }
    isLogin();*/
</script>
</body>
</html>
```
#### 05.for语句
for语句是一种更简洁的循环结构
格式如下：
>for（表达式1；表达式2；表达式3 )｛
	语句1；
	语句2……；
｝
语句3
>表达式在循环开始前无条件的求值一次，而表达式2在每次循环开始前求值。如果表达式2的值为真，则执行循环语句，否则终止循环。
表达式3在每次循环后被求值，然后再次判断。
```js
    /*
    for循环执行顺序
    1、首先执行语句1
    2、执行判断式2 如果成立（返回true）则执行代码块  如果不成立（返回false） 整个循环结束
    3、如果判断式成立去执行了代码块，执行完代码块 会去执行语句3
    4、语句3执行完成后  再次去执行判断式2
    5、重复第二个步骤
    */

    // 假设 弹出你好 总共弹出5次
    for (var i = 0; i < 5; i++) {
        console.log("nei hao a");
    }

    // 练习：定义一个变量a=5,让a执行5次，每次a加3。然后弹出a最终的值。
    var a = 5;
    for (var i = 0; i <5 ; i++) {
        a += 3;
    }
    console.log(a);
```
#### 06.for循环的练习
```js
    //1、求1到9的和
    // 1+2+3+4+5+6+7+8+9
    // 定义一个变量保存和  默认是0
    /*var num = 0;
    for (var i = 1; i < 10; i++) {
        num += i;
    }
    console.log(num);*/


    // 2、求1到100的和
    /*var num = 0;
    for (var i = 1; i < 101; i++) {
        num += i;
    }
    console.log(num);*/


    // 3、求1-99中的单数的和
    /*var num = 0;
    for (var i = 1; i < 100; i+=2) {
        num += i;
    }
    console.log(num)*/


    // 4、求1-99中是3的倍数的数字和
    /*var num = 0;
    for (var i = 3; i < 100; i+=3) {
        num += i;
    }
    console.log(num)*/

    /*var num = 0;
    for (var i = 0; i < 100; i++) {
        if (i % 3 == 0){
            num += i;
        }
    }
    console.log(num)*/


    // 5、定义一个v，当v等于0时，v进行3次自加1。否则v进行4次自加2
    /*var v = 3;
    if(v == 0){
        for (var i = 0; i <3 ; i++) {
            v++;
        }
    }else{
        for (var i = 0; i <4 ; i++) {
            v += 2;
        }
    }*/

    // 6、定义v＝3；对变量i由0到3进行遍历；当i 等于2时，v自加2；否则v自加3
    /*var v = 3;
    for (var i = 0; i < 4; i++) {
        if (i == 2){
            v += 2;
        }else{
            v += 3;
        }
    }*/
```
#### 07.for循环的应用
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>for循环应用</title>
</head>
<body>
    <ul id="box">
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
    </ul>
    <script>
        /*
         * 效果 对所有的li绑定点击事件  点击谁 让谁的背景颜色变成红色
         * 1、获取标签
         */

        // 1、获取标签
        var oBox = document.getElementById("box");
        var oLis = oBox.getElementsByTagName("li");

        /*oLis[0].onclick = function () {
            this.style.backgroundColor = "red";
        }
        oLis[1].onclick = function () {
            this.style.backgroundColor = "red";
        }
        oLis[2].onclick = function () {
            this.style.backgroundColor = "red";
        }
        oLis[3].onclick = function () {
            this.style.backgroundColor = "red";
        }
        oLis[4].onclick = function () {
            this.style.backgroundColor = "red";sd 
        }*/

       /* for (var i = 0; i < oLis.length; i++) {
            oLis[i].onclick = function () {
                this.style.backgroundColor = "red";
            }
        }*/


        /*
         * 效果 对偶数个数的（0 2 4 6 8 10）li绑定点击事件  点击谁 让谁的背景颜色变成红色
         * 1、获取标签
         */

        var oBox = document.getElementById("box");
        var oLis = oBox.getElementsByTagName("li");

        for (var i = 0; i < oLis.length; i += 2) {
            oLis[i].onclick = function () {
                this.style.backgroundColor = "red";
            }
        }
    </script>
</body>
</html>
```
#### 08.九九乘法算表
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>九九乘法算表</title>
</head>
<body>
<div id="box">

</div>
<script>
    var oBox = document.getElementById("box");
    for (var i = 1; i < 10; i++) {
        // 第一个for控制行的
        for (var j = 1; j <= i; j++) {
            // 第二个for 执行这一行的  签的乘数
            var math = j + "*" + i + "=" + j*i+" ";
            console.log(math)
            oBox.innerHTML = oBox.innerHTML + math;
        }
        // 在每一行执行结束后，添加一个换行
        oBox.innerHTML += "<br>";
    }


</script>
</body>
</html>
```
### 07.流程控制
使用break、label、continue、return语句可以中途改变分支结构、循环结构的流程方向，以提升程序的执行效率。return在函数中会做详细讲解
#### 01.label语句
在JS中，label语句可以为一行语句添加标签，以方便在复杂的结构中设置跳转目标。
语法如下：
    label:语句
>label可以是任意合法的标识符，然后使用冒号分割标签名与标签语句。
label和break语句配合使用，主要应用在循环结构、多分枝结构中，以便与跳出内层嵌套体。
```js
    var num=0;
    outermost:
        for(var i=0; i<10;i++){
            for(var j=0; j<10; j++){
                if(i==5 && j==5){
                    break outermost;
                }
                num++;
            }
        }
    console.log(num);
```
#### 02.break语句
break语句能够结束当前for、for/in、while、do/while或者switch语句的执行。同时break可以接受一个可选的标签名，来决定跳出的结构语句。
如果没有设置标签名，则跳出当前最内层结构。
```js
    //break 是立即退出循环 或 退出switch语句  执行循环后边的代码
    var  num =0 ;
    for ( var i=0 ; i<5 ; i++ ) {
        if ( i == 3 ) {
            break;
        }
        num++;
    }
    alert( num );//3



    var num=0;
    outermost:
        for(var i=0; i<10;i++){
            for(var j=0; j<10; j++){
                if(i==5 && j==5){
                    break outermost;
                }
                num++;
            }
        }
    console.log(num);

```
#### 03.continue语句
continue语句用在循环结构内，用于跳出本次循环中剩余的代码，并在表达式的值为真的时候，继续执行下一次循环。
可以接受一个可选的标签名，来决定跳出的循环语句。
```js
    
    var  num =0 ;
    for ( var i=0 ; i<5 ; i++ ) {
        if ( i == 3 ) {
            continue;
        }
        num++;
    }
    alert( num );//3



    var num=0;
    outermost:
        for(var i=0; i<10;i++){
            for(var j=0; j<10; j++){
                if(i==5 && j==5){
                    continue outermost;
                }
                num++;
            }
        }
    console.log(num);
```
### 08.异常处理
ECMA-262规范了7种错误类型。其中Error是基类，其他6种错误类型是子类，都继承了基类。Error类型的主要作用是自定义错误对象。
- Error：普通异常 。与thorw语句和try/catch语句一起使用，属性name可以读写异常类型，message属性可以读写详细的错误信息。
- EvalError：不正确使用eval()方法时抛出
- SyntaxError：出现语法错误时抛出
- RangeError：数字超出合法范围之抛出
- ReferenceError：读取不存在的变量时抛出
- TypeError：值的类型发生错误的时候抛出
- URIError：URI编码和解码错误时抛出
####01.try/catch/finally语句
try/catch/finally语句是异常处理语句
try{
    调试代码块
}
catch(e){
    捕获异常，并进行异常处理的代码块
}
finally{
    后期清理代码块
}

正常情况下，JS按顺序执行try子句中的代码，如果没有异常发生，将会忽略catch跳转到finally子句继续执行。
如果在try子句运行错误，或者使用throw语句主动抛出异常，则执行catch子句中的代码，同时传入一个参数，引用Error对象
```js
    // try catch 案例
    try{
        console.log(a);//当try中出现错误的时候，会直接进入catch执行
        console.log("我是try");
    }catch (e) {
        console.log("catch");
        console.log(e);//referenceError:a is not defined
        console.log(e.name);//referenceError
        console.log(e.message);//a is not defined
    }


    try{
        console.log("try");
        throw new Error("你是不是没有定义变量");
    }catch (e) {
        console.log("catch")
        console.log(e);
        console.log(e.name);
        console.log(e.message);
    }



    try{
        console.log("try");
        // throw new Error("你是不是没有定义变量");
    }catch (e) {
        console.log("catch")
        console.log(e);
        console.log(e.name);
        console.log(e.message);
    }finally {
        console.log('finally')
    }

    alert(1);

    // throw是抛出错误
    var a = 10;
    if(a > 4){
        // throw "你错啦吗？";
        // throw new TypeError("你的类型错误");
        var userError = "你今天犯错了，错误如下。。。。。。。。";
        throw new SyntaxError(userError);
    }
```
### 09.练习
#### 01.收银程序
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>收银程序</title>
</head>
<body>
<script>
    fz

    //输入商品的单价和数量
    var price = prompt("请输入单价");
    var count = prompt("请输入数量");

    //计算总价
    var sumPrice = price * count;

    //判断是否打折
    if (sumPrice >= 500){
        sumPrice *= 0.8;
    }

    //给用户说需要付多少钱
    var money = prompt("您本次消费"+sumPrice+"元，请付款(输入付钱的面额即可，稍等给您找零)");

    // 判断用户缴费是否足够，并找零
    if (money > sumPrice) {
        // 计算找零
        var reduceMoney = money - sumPrice;
        alert("找零" + reduceMoney + "元，请收好")
    }else{
        alert("钱不够！！！！")
    }

    alert("欢迎下次光临");
</script>
</body>
</html>
```
#### 02.ATM按键
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>ATM按键</title>
</head>
<body>
<script>
    var userPress = prompt("欢迎光临银行，请输入数字选择功能（1.查询余额，2.取钱，3.转账，4.退出）");
    switch (parseInt(userPress)) {
        case 1:
            search();
            break;
        case 2:
            drag();
            break;
        case 3:
            change();
            break;
        case 4:
            exit();
            break;
        default:
            alert("你丫看不懂提示么");
    }
    
    function search() {
        alert("正在查询余额");
    }
    function drag(){
        alert("正在取钱啊");
    }
    function change() {
        alert("正在转账")
    }
    function exit() {
        alert("正在退出")
    }
</script>
</body>
</html>
```
#### 03.买保险
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>买保险</title>
</head>
<body>
<script>
    /*
    * 公司给员工买保险（用户通过此程序查询自己是否符合条件）：
    * 只要结婚的都买
    * 没有结婚的男人 25岁以下不买
    * 没有结婚的姑娘 22岁以下不买
     */
    //输入是否结婚
    var isMarry = prompt("你结婚了吗？请输入yes和no");
    var age = prompt("您今年高寿啊");
    var sex = prompt("您性别是什么(man or woman)");
    if (isMarry === "yes"){
        alert("您放心做吧，公司给您提供免费的保险");
    }else if ((sex === "man" && age < 25) || (sex === "woman" && age < 22)){
        alert("自己回家买去吧");
    }else{
        alert("公司也给您买");
    }


</script>
</body>
</html>
```

## 六、函数
### 01.什么是函数
函数是一段被封装的代码，可以反复被调用。
在JS中，函数也可以是一个值、一个对像、还可以是一个表达式,因此函数可以赋值、可以运算、可以拥有属性和方法
JavaScript拥有函数式编程的很多特性和风格,灵活使用函数,可以编写出功能大、代码简洁、设计优雅的程序。
```js
    /*var yourGirlFri = {};
    yourGirlFri.name = "张三";
    yourGirlFri.sex = "女";
    yourGirlFri.age = "40";
    yourGirlFri.price = "388";

    var yourGirlFri = {};
    yourGirlFri.name = "李四";
    yourGirlFri.sex = "女";
    yourGirlFri.age = "18";
    yourGirlFri.price = "188";

    var yourGirlFri = {};
    yourGirlFri.name = "王大麻子";
    yourGirlFri.sex = "女";
    yourGirlFri.age = "12";
    yourGirlFri.price = "1200";*/

    //一段相同的代码重复执行  我们可以书写一个函数把代码包含起来  使用的时候 直接调用函数即可
    function yourGirlFri(name,sex,age,height) {
        var obj = {};
        obj.name = name;
        obj.sex = sex;
        obj.age = age;
        obj.height = height;
        return obj;
    }

    var girl1 = yourGirlFri("lily","男","19","180")
    var girl2 = yourGirlFri("王八八","女","100","190")
    var girl3 = yourGirlFri("王久久","女","90","110")

    console.log(girl1)
    console.log(girl2)
    console.log(girl3)
```
### 02.定义函数
#### 01.声明函数
- 在 Javascript中可以使用function语句声明函数。
>function funName ([args]){
    statements
}
- funName是函数名,与变量名一样都必须是JavaScript合法的标识符。
- 在函数名之后是一个由小括号包含的参数列表,参数之间以逗号分隔。参数是可选的,没有数量限制。
- 作为标识符,参数仅在函数体内被访问,参数是函数作用域的私有成员。调用函数时,通过为函数传递值,然后使用参数获取外部传入的值,并在函数体内干预函数的运行
- 在小括号之后是一个大括号,大括号内包含的语句就是函数体结构的主要内容。在函数体中，大括号号是必不可少的,缺少大括号, JavaScript将会抛出语法错误,
- var语句和function语句都是声明语句,它们声明的变量和函数都在JavaScript预编译时被解析,也被称为变量提升和函数提升。
```js
    //直接声明函数，可以直接提升
    fn1(1,2,3);
    function fn1(a,b,c) {
        console.log(a,b,c)
    }


    //函数只有定义在了其他函数中，才是局部的函数，否则都是全局的，在哪都能调用
    //ES5中，不允许 函数书写在非函数的代码块中
    /*fn2();//oh
    console.log(fn2);
    var a = 100;
    if (a > 10){
        function fn2() {
            alert("oh");
        }
    }
    fn2();//oh*/


    //函数也可以不书写名字，这种函数被称作为匿名函数
    /*function () {
        alert("heng")
    }*/

    //匿名函数的执行方法 1   自调用(分为直接扩住函数体调用、在函数前添加 ！~ + - 一元运算符 然后 添加小括号调用)
    (function (){
        alert("heng");
    })();

    !function (){
        alert("heng");
    }()

    //匿名函数的执行方法 2  赋值调用  （也被称作为函数表达式）  这种方法只能提升fn3  不能提升函数体

    var fn3 = function (){
        alert("heng");
    }
    fn3()
```
#### 02.构造函数
- 使用Function0)构造函数可以快速生成函数
- Functiono的参数类型都是字符串,p1-pn表示所创建函数的参数名称列表,body表示所创建函数的函数结构体语句,在body语句之间以分号分隔。
- 使用Function0构造函数不是很常用,因为一个函数体通常会恒含很多代码,如果将这些代研以一行字符串的形式进行传递,代码的可读性会很差。
```js
    var fn1 = new Function("console.log(111)");
    fn1();

    //以下两种传参方式都可以使用
    var fn2 = new Function("a","b","c","console.log(a+b+c)");
    var fn2 = new Function("a,b,c","console.log(a+b+c)");
    fn2(1,2,3);

```
#### 03.函数直接量
- 函数直接量也称为匿名函数,即函数没有函数名,仅包含函数关键字,参数和函数体,具体用法如下
`function (){}`
- 匿名函数就是一个表达式,即函数表达式,而不是函数结构的 sdk语句,可以把匿名函数作为值赋值给变量或者对象等等
- 当把函数结构作为一个值赋值给变量之后,变量就可以作为函数被调用,此时变量就指向那个匿名函数
- 匿名函数可以自己调用，比如加上小括号然后整体调用，或者在最欠扁添加!-+~等等一元操作符
```js
    // 把函数当做一个值
    /*function fn1() {
        console.log("fn1");
    }
    var fn2 = fn1;
    var fn3 = function (){
        console.log("匿名")
    }
    fn2();
    fn3();*/
    
    
    
    //函数也可以是一个对象
    function fn1() {
        alert("fn1");
    }
    fn1.name1 = "lily";
    fn1.sex = "nv";
    // fn1();
    alert(fn1.name1);
    alert(fn1.sex);

    //函数可以作为对象的某个方法
    var obj = {
        name :"lily",
        sex:"nan",
        say:function () {
            alert("aaaaaaaaa");
        },
        do:fn1
    }
    console.log(obj.name);
    console.log(obj.say());//undefined
    obj.do();
```
### 03.调用函数
JavasScipt供4种函数调用模式,函数调用,方法调用,使用call或apply动态调用(后边讲解),使用new间接调用(后边讲解)
```js
    //函数可以作为对象的某个方法
    var obj = {
        name :"lily",
        sex:"nan",
        say:function () {
            alert("aaaaaaaaa");
        },
        do:fn1
    }
    console.log(obj.name);
    console.log(obj.say());//undefined
    obj.do();
```
#### 01.函数调用
- 在默认状态下,函数是不会被执行的,使用小括号可以激活并执行函数。在小括号中可以包含零个或多个参数,参数之间通过逗号进行分隔（可以返回函数并调用）
####02.函数的返回值
- 函数提供两个接口与外界的交互，其中参数作为入口，接受外界的信息。返回值作为出口，把运算结果反馈给外界。
- 在函数体内,使用return语句可以设置函数的返回值。一旦执行返回语句,将停止函数的运行,并运算和返回返回后面的表达式的值
- 如果函数不包含return语句,则执行完函数体内每条语句后,h返回undefiend值。
- JavaScript是一种弱类型语言,所以函数对接收和输出的值都没有类型限制,JavaSeript也不会自动检测输入和输出值的类型
- 可以返回一个计算值 也可以返回多个值（使用对象或者数组）
```js
 function fn1(a,b){
        var sum = a + b;
        return sum;
        alert("计算完毕");
    }
    fn1(1,2);//如果不用变量接受，或者是不使用，那么这个返回值是看不到的
    console.log(fn1(1,2)+4);//7


    function fn1() {
        var a = 1;
        return function () {
            alert(a);
        }
    }
    fn1()();
    var b = fn1();
    console.log(b);
    a();


    function teacherMessage(name,age,sex) {
        alert("我的名字是"+name);
        alert("我的年龄是"+age);
        alert("我的性别是"+sex);
    }

    var teacher1 = {
        name:"lily",
        age:"18",
        sex:"nv"
    }
    var teacher2 = {
        name:"lily1",
        age:"128",
        sex:"nan"
    }
    function teacherMessage(obj) {
        alert("我的名字是"+obj.name);
        alert("我的年龄是"+obj.age);
        alert("我的性别是"+obj.sex);
    }
    teacherMessage(teacher1);


    function fn1() {
        var a = 1;
        return;//返回的是undefined
        alert(2);
    }

    console.log(fn1());
```
#### 03.方法调用
- 当一个函数被设置为对象的属性值时,称之为方法,使用点语法可以调用一个方法


### 04.函数参数
- 参数是函数对外练习的唯一入口，用户只能通过参数来控制函数的运行。
#### 01.形参和实参
- 形参：在定义函数时，声明的参数变量仅在函数内部可见
- 实参：在调用函数时，实际传入的值
- 一般情况下，函数的实参和形参的数量应该相同，但是JS并没有这样的要求。可以不相同
- 如果函数的实参数量少于形参数量，那么多出来的形参会默认会undefined
- 如果函数实参数量多余形参数量，那么多出来的实参就不能通过形参访问。函数忽略掉多余的实参。
- 可以设定形参默认值或者判断给值
```js
    function f(a,b) {

    }
    f(1,2);


    function f2(a,b,c) {
        console.log(a,b,c);//1 2 undefined
        console.log(typeof c);//undefined
    }
    f2(1,2);

    function f3(a,b,c) {
        console.log(a,b,c)
    }
    f3(1,2,3,4,5,6,7)

    //书写一个函数 计算 三个值的和
    /*function add(a,b,c) {
        return a+b+c;
    }

    console.log(add(1, 2));//NaN*/


    //直接给函数形参默认值
    /*function add(a,b,c=0) {
        return a+b+c;
    }
    console.log(add(1, 2));//NaN*/

    //判断参数是否存在，否则给出默认值
    function add(a,b,c) {
        c = typeof c === "undefined" ? 0 : c;
        typeof c === "undefined" ? c = 0 : c;
        return a+b+c;
    }
    console.log(add(1, 2));//NaN
```
#### 02.获取参数个数
- 使用arguments对象的length属性可以获取函数的实参个数。
- argument对象只能在函数内可见,因此arguments.legth也只能在函数体内使用。
- 使用函数对象的length属性可以获取函数的形参个数,该属性为只读属性,在函数体内,体外都可以使用
####03.使用arguments对象
- arguments对象表示函数的实参集合,仅能够在函数体内可见,并可以直接访间。
- 参数对象是一个伪类数组,不能够继承Anray的原型方法。可以使用数组下标的形式访问每个实参,如参数[0]表示第一个实参
- 通过修改length属性值，可以改变函数的实参个数。
```js
    function fn1(a,b,c) {
        console.log(arguments.length);//获取实参的个数
    }
    fn1(1,2,3,4)

    //输入一组数字，求平均值的函数
    function f() {
        //先获取到所有的实参 使用arguments
        var sum = 0;
        for (var i = 0; i < arguments.length; i++) {
            sum += arguments[i];
        }
        return sum / arguments.length;
    }

    console.log(f(12, 34, 54, 32, 100, 98, 45, 34, 12));



    // 直接使用函数对象的length属性，就可以获取到函数的形参个数
    function f3(a,b,c) {
        console.log(f3.length);//3
    }
    f3(1,2,3,4,5,6);



    // 检测函数的形参和实参是否一致，如果不一致，则抛出错误
    /*function f4(a,b,c,d) {
        if (arguments.length != f4.length) {
            throw new Error("参数不一致");
        }else{
            alert("go")
        }
    }
    f4(1,2,3,4,5)*/
```
#### 04.使用callee
callee是arguments对象的属性，它引用当前argument对象所在的函数，使用该属性可以在函数体内调用自身。
```js
    // 检测函数的形参和实参是否一致，如果不一致，则抛出错误
    /*function f4(a,b,c,d) {
        if (arguments.length != arguments.callee.length) {
            throw new Error("参数不一致");
        }else{
            alert("go")
        }
    }
    f4(1,2,3,4,5)*/

    var a = 0;
    (function (){
        a++;
        alert(1);
        if (a > 1){
            return;
        }
        arguments.callee()
    })();
```
#### 05.函数的练习
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>函数的练习</title>
</head>
<body>
<button id="red">红色</button>
<button id="green">绿色</button>
<button id="blue">蓝色</button>
<button id="pink">粉色</button>

<script>
    /*
    * 当点击不同的按钮的时候 让页面加载相应的颜色
    * 改变屏幕的颜色 就是控制body的背景颜色
     */
    var oBody=document.getElementsByTagName("body")[0];
    var oRed = document.getElementById("red");
    var oGreen = document.getElementById("green");
    var oBlue = document.getElementById("blue");
    var oPink = document.getElementById("pink");

    function changeColor(col){
        oBody.style.backgroundColor = col;
    }
    oRed.onclick=function () {
        changeColor("red");
    }
    oGreen.onclick=function () {
        changeColor("green");
    }
    oBlue.onclick=function () {
        changeColor("blue");
    }
    oPink.onclick=function () {
        changeColor("pink");
    }

</script>
</body>
</html>
```

### 05.函数作用域
#### 01.变量作用域
变量作用域（scope）是指变量在程序中可以访问的有效范围。也称为变量的可见性。分为全局变量和局部变量
- 全局变量：变量在整个页面中都是可见的，可以被自由的访问
- 局部变量，变量仅能在声明的函数内部可见，函数外是不允许访问的。
- var声明的作用与是按照函数划分的
```js
    /* var a = 1;
        function f() {
            console.log(a);
        }
        f();
    */

    function f2 (){
        var a = 2;
        function f3() {
            console.log(a);
        }
        f3();
    }
    // f3();//f3是局部函数 外部使用不了的
    f2();
    console.log(a);
```
#### 02.执行上下文和活动对象
01.什么是执行上下文

- JavaScript代码是按顺序从上到下被解析的,当然JS引擎并非逐行地分析和执行代码,而是去分析和执行。当执行一段代码时,先进行预处理,如变量提升、函数提升等。
- JavaScript可执行代码包括3种类型:全局代码、函数代码、eval代码。每执行一段可执行代码,都会创建对应的执行上下文。在脚本中可能存在大量的可执行代码段,所以 JavaScript引擎先创建执行上下文栈,来管理脚本中所有执行上下文
- 执行上下文是一个专业术语,比较抽象,实际上就是在内存中开辟的一块独立运行的空间。执行上下文栈相当于一个数组,数组元素就是独立的执行上下文区域。
- 当 JavaScript开始解释程序时,最先遇到的是全局代码,因此在初始化程序的时候,首先向执行上下文栈压入一个全局执行上下文,并且只有当整个应用程序结束的时候,全局执行上下文才被清空。
- 当执行一个函数的时候,会创建一个函数的执行上下文,并且压入到执行上下文栈,当函数执行完毕,会将函数的执行上下文从栈中弹出
- 每个执行上下文都有3个基本属性:变量对象、作用域链和this。

02.全局上下文的变量对象

- 全局上下文的变量对象,初始化是全局对象（window）
- 全局对象（window）是预定义的对象,作为 JavaScript的全局函数和全局属性的占位符,在客户端 JavaScript中,全局对象是 window对象.通过全局对象，可以访问其他所有预定义的对象。

03.函数上下文的变量对象

- 变量对象是 ECMAScript规范术语。在一个执行上下文中,变量对象才被激活,只有激活的变量对象,其各种属性才能被访问
- 函数执行上下文的代码处理可以分成两个阶段:分析和执行,简单说明如下
>执行过程
- 进入执行上下文。当进入执行上下文时,不会执行代码,只进行分析。此时变量对象包括函数的所有形参(如果是函数上下文)
- 函数声明—由名称和对应值(函数对象)组成的一个变量对象的属性被创建。如果变量对象已经存在相同名称的属性,则会完全替换这个属性
- 变量声明 由名称和对应值( undefined)组成的一个变量对象的属性被创建。如果变量名称与已经声明的形参或函数相同,则变量声明不会覆盖已经存在的这类属性
- 执行代码
#### 03.作用域链
- 当代码在一个环境中执行时,会创建变量对象的一个作用域链( scope chain),作用域链的用途,是保证对执行环境有权访问的所有变量和函数的有序访问。
- 作用域链的前端,始终都是当前执行的代码所在环境的变量对象。
- 全局执行环境的变量对象始终都是作用域链中的最后一个对象。
- 标识符解析是沿着作用域链一级一级地搜索标识符的过程。搜索过程始终从作用域链的前端开始
- 然后逐级地向后回溯,直至找到标识符为止(如果找不到标识符,通常会导致错误发生)
#### 04.this和调用对象
javascript函数的作用域是静态的,但是函数的调用却是动态的,由于函数可以在不同的运行环境内执行,因此 JavaScript在函数体内定义了this关键字,用来获取当前的运行环境。
this是一个指针型变量,它动态引用当前的运行环境,具体来说,就是调用函数的对象。
this永远指向其所在函数的调用者，如果没有所有者则指向全局对象window
```js
//obj.f在上面代码中,obj.f表示在obj对象上调用f函数,则调用对象为obj,此时this就指向obj,this.x就等于obj.x,即返回结果为2
//若把obj.f赋值给变量f1,然后在全局上下文中调用们函数,则f函数体的运行环境在全局上下文中执行,此时this就指向 window, this.x就等于 window.x,即返回结果为1
var x = 1;
var obj = {
    f:function(){
        console.log(this.x)
    },
    x:2
}
obj.f();
var f1 = obj.f;
f1();


//在上面代码中,小括号左侧都是一个表达式,表达式的值都是obj.f
var x = 1;
var obj = {
    f:function(){
        console.log(this.x);
    }
    x:2,
}
  
(obj.f = obj.f)();//正确理解“运行环境”obj.f=obj.f是赋值表达式,把obj.f赋值给obj.f,obj.f是一个地址,把地址赋值给obj.f属性,表达式的运行环境发生在全局上下文中,所以此时函数f内的this就指向了全局上下文的调用对象 window
(false||obj.f)();//逻辑表达式,左侧操作数为false,则运算右侧操作数,返回obj.f的值,即引用地址。由于这个逻辑表达式运算发生在全局作用域内,此时的f函数内this就指向了全局对象
(obj.f,obj.f);//逗号运算表达式,逗号左侧和右侧的obj.f都是一个地址,都被运算一次,最后返回第2个操作数的值,即返回引用地址。由于这个操作发生在全局作用域内,所以f函数内this也指向了全局对象
(obj.f)//his指向obj对象,因为小括号不是一个运算符,它仅是一个逻辑分隔符,不执行运算,不会产生运行环境,当使用小括号调用函数时,此时生成的运行环境就是obj
```

#### 05.函数练习
```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
</head>
<body>
	<script>


	//demo1
		
		/*var v = "hello";
		(function(){
			alert(v);//
			var v = "world";
		})();
		alert(v);//*/

		/*var v;
		v = "hello";//全局作用域v变成hello
		(function(){
			var v;//声明局部变量v  外边的hello是不可能再进来了
			alert(v);//  声明了 没有赋值 undefined
			v = "world";//修改的是局部变量
		})();
		alert(v);//*/





	//demo2
		/*(function(){
			alert(a+b+c);//NaN
			var a = "1";
			var f = function(){};
			var b = "2";
			var c = "3";
		})();*/



		

	//demo3
		//函数声明是整体提升
		//函数表达式 只提升声明的变量  不会带着函数体一起提升
		/*(function(){
			f2();//1
			f1();//f1 is not a function
			var f1 = function(){
				alert(2)
			};
			function f2(){
				alert(1);
			}
		})();*/

		/*(function(){
			function f2(){
				alert(1);
			}
			var f1;
			f2();//1
			f1();//f1是undefined  不是函数 报错 f1不是一个函数
			f1 = function(){
				alert(2)
			};
		})();*/




	//demo4
		/*var a = 1;//全局
		function outer(){ 
			var b = 2; 
			function inner(){ 
				var c = 4; 
				alert(a); //沿着作用域链向上寻找 直到找到全局a  所以是1
			} 
			inner(); //调用inner函数 
		} 
		outer(); //调用outer函数*/

		 


	//demo5
		/*var a = 1;
		function check(){ 
			a = 100;//是把全局a变成了100
			alert(a); //100
		} 
		check(); 
		alert(a);//全局的a 已经变成了 100*/


	//demo6
		/*var v = "hello";
		if(true){
			alert(v);//hello 这里仍然是全局作用域
			var v = "world";//js允许多次var声明同一个变量  覆盖操作
		}
		alert(v);//world*/


	

	//demo7
		/*function rain(){
			var x = 1; 
			function man(){ 
				x = 100; //把父级作用域的x变成了100
			} 
			man(); 
			alert( x );//100  父级的x
		} 
		rain();*/



	//demo8
		/*var x = 1;
		function rain(){
			alert( x );//undefined 当前作用域声明了x  所以不用全局的  但是没赋值 udefined
			var x = 'man'; 
			alert( x );//'man'
		} 
		rain()*/


	//demo9
	// 	当作用域去寻找某个变量  直到全局都没有找到的话，就默认这个变量是在全局声明的
		/*function rain(){
			x = 100;
		}
		rain();
		alert( x );//100*/
 





	

	//demo10
		/*var t='a';
		function test2(){
			alert(t);//undefined
			var t='b';
			alert(t);//"b"
		}
		test2();*/




	//demo11
		/*var t='a';
		function test2(){
			alert(t);//a
			t='b';
			alert(t);//'b'
		}
		alert(t);//'a'
		test2();
		alert(t);//'b'*/

	//demo12
		/*var a="Hello";
		function test(){  
			alert(a);//hello
			a="World";
			alert(a);//world
		}
		test();*/


	//demo13
		/*var a =1;
		function test(){
			alert(a);//undefined
			a=4;
			alert(a)//4
			var a=2;
			alert(a);//2
		}
		test();
		alert(a);//1*/

		 
	</script>
</body>
</html>
```

## 七.事件类型
### 01.获取标签
```html
<!DOCTYPE html> t
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>获取标签</title>
</head>
<body>
    <ul id="box">
        <li></li>
        <li></li>
        <li></li>
        <li></li>
    </ul>
    <ul>
        <li class="li1" name="oli"></li>
        <li class="li1"></li>
    </ul>
    <script>
        // 1、通过id获取标签 id是唯一的  所以通过id获取的标签也是唯一的
        //完美兼容

        var oBox = document.getElementById("box");
        console.log(oBox);//得到整个元素
        oBox.style.backgroundColor = "red";

        // id如果没有获取，那么仍然可以拿着id名来使用，因他是唯一的。但是不建议这样书写
        box.style.backgroundColor = "red";


        //2、通过标签名获取（完美兼容）
        // 无论页面有1个还是多个，通过标签名获取的元素一定是复数格式的
        //获取的是一个集合 这个集合拥有length属性  是一个类数组（伪数组）的对象
        var oLis = document.getElemerntsByTagName("li");
        console.log(oLis);

        // 使用：
        /*通过标签名获取的对象  要么在使用的时候添加下标，要么在获取的时候添加下标
        因为使用的时候，只能拿一个元素去使用*/
        // oLis.style.backgroundColor = "green";//报错，无法直接对一个集合设置style
        //中括号 给集合添加下标，选中要控制第几个，下标从0开始
        oLis[0].style.backgroundColor = "green";
        oLis[1].style.backgroundColor = "green";
        oLis[2].style.backgroundColor = "green";
        oLis[3].style.backgroundColor = "green";

        /*伪数组：1、键名是从0开始按照升序一次排列  2、拥有length属性是对象的长度
        {0:"lily",1:"lucy",2:"xiaowang",length:3}//伪数组

        ["lily","lucy","xiaowang"]*/

        //3、通过标签名  获取元素的时候就添加上下标 那每一次就只能获取一个了
        var oLis1 = document.getElementsByTagName("li")[0];
        oLis1.style.backgroundColor = "pink";



        // 4、目前通过标签名获取元素，有局限性  只能一次获取所有的li，我们可以对标签名获取提供限制
        //比如获取 box中 所有的 li元素
        /*var oBox = document.getElementById("box");
        var oBox_lis = oBox.getElementsByTagName("li");
        console.log(oBox_lis);*/

        /*var oBox = document.getElementsByTagName("ul")[0];
        var oBox_lis = oBox.getElementsByTagName("li");
        console.log(oBox_lis);*/


        // 5、通过类名来获取元素（不兼容IE678）i
        //获取的是一个复数  使用和通过标签名获取的对象 使用方法一致

        // IE8不认识此方法：对象不支持“getElementsByClassName”属性或方法
        // var oLi1 = document.getElementsByClassName("li1");
        // oLi1[0].style.backgroundColor = "green";


        // 6、通过Name属性获取元素（几乎不使用）
            //获取的是一个复数 集合
            // 兼容性：针对ie：通过Name获取 只能获取到表单元素  不支持其他元素通过name获取
                    //其他浏览器可用
        /*var oLi = document.getElementsByName("oli");
        oLi[0].style.height = "300px";*/
    </script>
</body>
</html>
```
### 02.失去和获取焦点事件
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>事件</title>
</head>
<body>
<!--    模拟一个表单输入内容提示-->
    <input type="text" value="请输入电话号码" id="tel">
<script>
    /*
        模拟placeholder
        当用户单击表单开始输入时  表单内容为空
        当用户没有输入 或者刚刷新页面的时候，表单提示为“请输入你的电话号码”

        1、获取焦点事件
        2、判断 当表单内是“请输入电话号码”的时候，清空value值 让用户开始输入
        3、书写失去焦点事件
        4、判断 表单内的值是空（也就是用户没有输入任何内容的时候） 把提示重新书写进入

     */
    var oTel = document.getElementById("tel");
    // 1、获取焦点事件
    oTel.onfocus = function () {
        // 2、判断 当表单内是“请输入电话号码”的时候，清空value值 让用户开始输入
        if(oTel.value == "请输入电话号码"){
            // 清空value值
            oTel.value = "";
        }
    }
    // 3、书写失去焦点事件
    oTel.onblur = function () {
        // 4、判断 表单内的值是空（也就是用户没有输入任何内容的时候） 把提示重新书写进入
        if(oTel.value == ""){
            // 把提示重新书写进入
            oTel.value = "请输入电话号码";
        }
    }

</script>
</body>
</html>
```

### 03.点击事件
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>点击事件</title>
    <style>
        #box{
            width: 300px;
            height: 200px;
            background: pink;
        }
    </style>
</head>
<body>
    <div id="box">我是box</div>
    <script>
        var oBox = document.getElementById("box");
        // 当在一个元素上按下鼠标  并又抬起的时候 才会触发click事件
        //右键也可能触发，但是右键的点击有专门的的事件 oncontextmenu
        oBox.onclick = function () {
            // alert(1);
        }

        // 右键事件  按下 并抬起的时候 弹出
        oBox.oncontextmenu=function(){
            alert(2);

            //取消默认右键的菜单弹出  取消默认事件 写在最后
            return false;
        }

        //双击事件
        oBox.ondblclick = function () {
            alert("用户双击");
        }
    </script>
</body>
</html>
```
### 04.点击事件练习
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>点击事件</title>
    <style>
        #box{
            width: 300px;
            height: 200px;
            background: pink;
        }
    </style>
</head>
<body>
    <div id="box">我是box</div>
    <script>

        /*
           * 效果要求：
           * 用户点击box  第一次点击变成红色背景 第二次变成粉色  。。。依次循环(开关的思想)
           * (开关的思想) 定义一个变量  保存当前的状态  然后每次点击后 判断 并把开关给改变了
           * 1、绑定点击事件
           * 2、定义一个开关  保存当前的状态
           * 3、事件发生后，判断当前的状态，如果是粉色则 变红  如果是红色 则变粉
           * 4、改变完成以后，改变开关的状态
         */
        var oBox = document.getElementById("box");
        // 2、定义一个开关  保存当前的状态
        var flag = true;//我们自定义，当flag为true的时候 说明现在是粉色  那么为false就是红色
        // 1、绑定点击事件
        oBox.onclick = function () {
            // 3、事件发生后，判断当前的状态，如果是粉色则 变红  如果是红色 则变粉
            if (flag){
                oBox.style.backgroundColor = "red";
                // 改变完成以后，改变开关的状态(简写在下边)
                // flag = false;
            }else{
                oBox.style.backgroundColor = "pink";
                // 改变完成以后，改变开关的状态(简写在下边)
                // flag = true;
            }
            // 每次点击完都让flag取反就可以  不用再判断中依次书写
            flag = ! flag;
        }
    </script>
</body>
</html>
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>点击事件</title>
    <style>
        #box{
            width: 300px;
            height: 200px;
            background: pink;
        }
    </style>
</head>
<body>
    <div id="box">我是box</div>
    <script>

        /*
           * 效果要求：
           * 用户点击box  第一次点击变成红色背景 第二次变成粉色  。。。
           * 取余运算的方法（定义一个变量，给一个初始值。每次点击都让这个变量累加  每次点击的让变量对2取余（因为目前效果是两种状态）来判断当前该显示什么颜色）
           * 1、绑定点击事件
           * 2、定义一个累加器  保存当前的状态
           * 3、事件发生后，判断当前的状态，如果是粉色则 变红  如果是红色 则变粉
           * 4、改变完成以后，改变开关的状态
         */
        var oBox = document.getElementById("box");
        // 2、定义一个累加器  保存当前的状态
        var num = 0;//每次点击都让这个变量累加  每次点击的让变量对2取余来判断
        // 1、绑定点击事件
        oBox.onclick = function () {
            // 3、事件发生后，判断当前的状态，如果是粉色则 变红  如果是红色 则变粉
            // 如果余0 那么代表是默认粉色
            if (num % 2 == 0){
                oBox.style.backgroundColor = "red";
            }else{
                oBox.style.backgroundColor = "pink";
            }
            // 改变完成以后，改变开关的状态
            num ++;
        }
    </script>
</body>
</html>
```

### 05.剩余字数练习
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>检测剩余字数</title>
    <style>
        textarea{
            border: 1px solid #ccc;
            outline: none;
        }
    </style>
</head>
<body>
    <textarea id="text" cols="30" rows="10" ></textarea>
    <p>还剩余 <span id="reduce">100</span> 个字</p>
    <script>
        /*
         * 用户在表单中输入内容，剩余字数减少，
         * 当剩余字数减少到负数的时候 把提示字数变成红色
         *
         * 1、获取标签
         * 2、书写键盘抬起事件 当抬起的时候 去计算剩余字数
         * 3、获取表单输入的长度
         * 4、计算剩余的字数是多少
         * 5、把计算好的剩余字数给到 reduce标签中
         * 6、检测剩余字数 小于0的时候，让标签变红  并且让textarea的边框变红
         * 7、当用户把字数重新减小，然后样式变成正常
         */
        // 1、获取标签
        var oReduce = document.getElementById("reduce");
        var oText = document.getElementById("text");

        // 2、书写键盘抬起事件 当抬起的时候 去计算剩余字数
        oText.onkeyup = function () {
            // 3、获取表单输入的长度
            var oTextLen = oText.value.length;
            // console.log(oTextLen);
            // 4、计算剩余的字数是多少
            var reduceTextNum = 100 - oTextLen;
            // 5、把计算好的剩余字数给到 reduce标签中
            oReduce.innerHTML = reduceTextNum;
            // 6、检测剩余字数 小于0的时候，让标签变红  并且让textarea的边框变红
            if (reduceTextNum < 0){
                oReduce.style.color = "red";
                oText.style.border = "1px solid red";
            }else{
                // 7、当用户把字数重新减小，然后样式变成正常
                oReduce.style.color = "#000";
                oText.style.border = "1px solid #ccc";
            }

        }
        

    </script>
</body>
</html>
```

### 06.input和change事件
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>input和change事件</title>
</head>
<body>
    <input type="text" id="ipt">
    <span id="text"></span>
    <script>
        /*
        * 模拟 数据双向绑定效果
        * 当用户在input中输入内容的时候  span中的内容跟着改变
        *
        * 1、获取标签
        * 2、绑定事件  当用户输入的时候触发
        *   oninput事件-->表单内容只要发生改变就会实时触发
        *   onchange事件 -->失去焦点 并且表单内容发生改变 才会触发
        * 3、获取输入的内容 并赋值给text
         */

        // 1、获取标签
        var oIpt = document.getElementById("ipt");
        var oText = document.getElementById("text");

        // 2、绑定事件  当用户输入的时候触发
        oIpt.oninput = function () {
            alert(1);
            // 3、获取输入的内容 并赋值给text
            oText.innerHTML = oIpt.value;
        }

    </script>
</body>
</html>
```

### 07.按下抬起事件
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>按下抬起事件</title>
    <style>
        #box{
            width: 200px;
            height: 200px;
            background: red;
        }
    </style>
</head>
<body>
    <div id="box">

    </div>
    <script>
        /*
        * 鼠标在元素上 按下 元素变成黄色  抬起 变成红色
        * onmousedown  鼠标按下事件
        * onmouseup  鼠标抬起事件
         */

        var oBox = document.getElementById("box");
        oBox.onmousedown = function () {
            oBox.style.backgroundColor = "yellow";
        }
        oBox.onmouseup = function () {
            oBox.style.backgroundColor = "red";
        }
    </script>
</body>
</html>
```
### 08.鼠标移入移出事件
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>鼠标移入移出事件</title>
    <style>
        #box{
            width: 300px;
            height: 300px;
            background: #2ba5eb;
            overflow: hidden;
        }
        #box p{
            background: #1eff0a;
            color: #fff;
            text-align: center;
            height: 100px;
            line-height: 100px;
        }
    </style>
</head>
<body>
    <div id="box">
        <p>我是第一个p标签</p>
        <p>我是第二个p标签</p>
    </div>
    <script>
        /*
         * 当鼠标移入box  让box 颜色发生变化   移出再还原 ， 只要鼠标在元素中移动  就一直打印 欢迎光临
         *
         * onmouseover 和 onmouseout 可以触发事件的冒泡（旧的，大多数时候不适用）
         * onmouseenter 和 onmouseleave 不会触发事件的冒泡 新的  兼容性良好
         *
         * onmousemove -->鼠标移动事件   (实时触发  只要移动就会触发)
         */

        /*var oBox = document.getElementById("box");
        oBox.onmouseover = function(){
            console.log("进去");
            oBox.style.backgroundColor = "red";
        }
        oBox.onmouseout = function () {
            console.log("出来");
            oBox.style.backgroundColor = "#2ba5eb";
        }*/

        var oBox = document.getElementById("box");
        oBox.onmouseenter = function(){
            console.log("进去");
            oBox.style.backgroundColor = "red";
        }
        oBox.onmouseleave = function () {
            console.log("出来");
            oBox.style.backgroundColor = "#2ba5eb";
        }

        oBox.onmousemove = function () {
            console.log("欢迎光临");
        }
    </script>
</body>
</html>
```

## 八.TAB切换
###01.选项卡切换页面结构
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>选项卡切换页面结构</title>
    <link rel="stylesheet" href="reset.css">
    <style>
        #outer{
            width: 606px;
            margin: 0 auto;
            border: 1px solid #2ba5eb;
        }
        #title{
            overflow: hidden;
        }
        #title>h3{
            width: 200px;
            border: 1px solid #ccc;
            height: 50px;
            text-align: center;
            line-height: 50px;
            color: #333;
            float: left;
        }
        #con{

        }
        #con>li{
            width: 606px;
            height: 300px;
            text-align: center;
            line-height: 300px;
            font-size: 40px;
            font-weight: bold;
            display: none;
        }
    </style>

</head>
<body>
    <div id="outer">
        <div id="title">
            <h3>标题一</h3>
            <h3>标题二</h3>
            <h3>标题三</h3>
        </div>
        <ul id="con">
            <li>内容一</li>
            <li>内容二</li>
            <li>内容三</li>
        </ul>
    </div>

    <script>
        /*
            *选项卡切换
         */
    </script>
</body>
</html>
```
###02.基础方法实现1
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>选项卡切换页面结构</title>
    <link rel="stylesheet" href="reset.css">
    <style>
        #outer{
            width: 606px;
            margin: 0 auto;
            border: 1px solid #2ba5eb;
        }
        #title{
            overflow: hidden;
        }
        #title>h3{
            width: 200px;
            border: 1px solid #ccc;
            height: 50px;
            text-align: center;
            line-height: 50px;
            color: #333;
            float: left;
        }
        #con{

        }
        #con>li{
            width: 606px;
            height: 300px;
            text-align: center;
            line-height: 300px;
            font-size: 40px;
            font-weight: bold;
            display: none;
        }
    </style>

</head>
<body>
    <div id="outer">
        <div id="title">
            <h3>标题一</h3>
            <h3>标题二</h3>
            <h3>标题三</h3>
        </div>
        <ul id="con">
            <li>内容一</li>
            <li>内容二</li>
            <li>内容三</li>
        </ul>
    </div>

    <script>
        /*
            *选项卡切换
         */
        var oTitle = document.getElementById("title");
        var oCon = document.getElementById("con");
        var oH3s = oTitle.getElementsByTagName("h3");
        var oLis = oCon.getElementsByTagName("li");

        // 1、默认标题一是被选中的  默认内容一是显示的
        oH3s[0].style.backgroundColor = "red";
        oH3s[0].style.color = "#fff";

        oLis[0].style.display = "block";


        // 分别对三个标题绑定点击事件，让对应的内容显示
        oH3s[2].onclick = function () {
            //让当前点击的显示特殊样式
            oH3s[2].style.backgroundColor = "red";
            oH3s[2].style.color = "#fff";
            //让其他的显示默认样式
            oH3s[0].style.backgroundColor = "#fff";
            oH3s[0].style.color = "#333";

            oH3s[1].style.backgroundColor = "#fff";
            oH3s[1].style.color = "#333";

            //让当前点击的元素对应的内容显示
            oLis[2].style.display = "block";

            //让不是当前点击的元素对应的内容隐藏
            oLis[1].style.display = "none";
            oLis[0].style.display = "none";
        }
        // 分别对三个标题绑定点击事件，让对应的内容显示
        oH3s[1].onclick = function () {
            //让当前点击的显示特殊样式
            oH3s[1].style.backgroundColor = "red";
            oH3s[1].style.color = "#fff";
            //让其他的显示默认样式
            oH3s[0].style.backgroundColor = "#fff";
            oH3s[0].style.color = "#333";

            oH3s[2].style.backgroundColor = "#fff";
            oH3s[2].style.color = "#333";

            //让当前点击的元素对应的内容显示
            oLis[1].style.display = "block";

            //让不是当前点击的元素对应的内容隐藏
            oLis[2].style.display = "none";
            oLis[0].style.display = "none";
        }
        // 分别对三个标题绑定点击事件，让对应的内容显示
        oH3s[0].onclick = function () {
            //让当前点击的显示特殊样式
            oH3s[0].style.backgroundColor = "red";
            oH3s[0].style.color = "#fff";
            //让其他的显示默认样式
            oH3s[2].style.backgroundColor = "#fff";
            oH3s[2].style.color = "#333";

            oH3s[1].style.backgroundColor = "#fff";
            oH3s[1].style.color = "#333";

            //让当前点击的元素对应的内容显示
            oLis[0].style.display = "block";

            //让不是当前点击的元素对应的内容隐藏
            oLis[1].style.display = "none";
            oLis[2].style.display = "none";
        }
    </script>
</body>
</html>
```
###03.基础方法2
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>选项卡切换页面结构</title>
    <link rel="stylesheet" href="reset.css">
    <style>
        #outer{
            width: 606px;
            margin: 0 auto;
            border: 1px solid #2ba5eb;
        }
        #title{
            overflow: hidden;
        }
        #title>h3{
            width: 200px;
            border: 1px solid #ccc;
            height: 50px;
            text-align: center;
            line-height: 50px;
            color: #333;
            float: left;
        }
        #con{

        }
        #con>li{
            width: 606px;
            height: 300px;
            text-align: center;
            line-height: 300px;
            font-size: 40px;
            font-weight: bold;
            display: none;
        }
        #title>.active{
            background-color: red;
            color: #fff;
        }
        #con>.show{
            display: block;
        }
    </style>

</head>
<body>
    <div id="outer">
        <div id="title">
            <h3 class="active">标题一</h3>
            <h3>标题二</h3>
            <h3>标题三</h3>
        </div>
        <ul id="con">
            <li class="show">内容一</li>
            <li>内容二</li>
            <li>内容三</li>
        </ul>
    </div>

    <script>
        /*
            *选项卡切换
         */
        var oTitle = document.getElementById("title");
        var oCon = document.getElementById("con");
        var oH3s = oTitle.getElementsByTagName("h3");
        var oLis = oCon.getElementsByTagName("li");

        // 分别对三个标题绑定点击事件，让对应的特殊类名给这个元素就可以
        oH3s[2].onclick = function () {
            // 给元素设置类名使用className属性
            oH3s[2].className = "active"
            oH3s[0].className = ""
            oH3s[1].className = ""

            oLis[2].className = "show"
            oLis[0].className = ""
            oLis[1].className = ""

        }
        oH3s[0].onclick = function () {
            // 给元素设置类名使用className属性
            oH3s[0].className = "active"
            oH3s[2].className = ""
            oH3s[1].className = ""

            oLis[0].className = "show"
            oLis[2].className = ""
            oLis[1].className = ""

        }
        oH3s[1].onclick = function () {
            // 给元素设置类名使用className属性
            oH3s[1].className = "active"
            oH3s[0].className = ""
            oH3s[2].className = ""

            oLis[1].className = "show"
            oLis[0].className = ""
            oLis[2].className = ""

        }

    </script>
</body>
</html>
```
###04.className
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>className</title>
    <style>
        .con{
            width: 200px;
            height: 200px;
        }
        .red{
            background-color: red;
        }
        .blue{
            background-color: blue;
        }
    </style>
</head>
<body>
    <button id="btn">点击</button>
    <div class="con red" id="con"></div>
    <script>
        var oBtn = document.getElementById("btn");
        var oCon = document.getElementById("con");
        oBtn.onclick=function () {
            // className是直接替换原来的类名
            console.log(oCon.className)
            oCon.className += " blue";
        }
    </script>
</body>
</html>
```
###05.基础方法3
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>选项卡切换页面结构</title>
    <link rel="stylesheet" href="reset.css">
    <style>
        #outer{
            width: 606px;
            margin: 0 auto;
            border: 1px solid #2ba5eb;
        }
        #title{
            overflow: hidden;
        }
        #title>h3{
            width: 200px;
            border: 1px solid #ccc;
            height: 50px;
            text-align: center;
            line-height: 50px;
            color: #333;
            float: left;
        }
        #con{

        }
        #con>li{
            width: 606px;
            height: 300px;
            text-align: center;
            line-height: 300px;
            font-size: 40px;
            font-weight: bold;
            display: none;
        }
        #title>.active{
            background-color: red;
            color: #fff;
        }
        #con>.show{
            display: block;
        }
    </style>

</head>
<body>
    <div id="outer">
        <div id="title">
            <h3 class="active">标题一</h3>
            <h3>标题二</h3>
            <h3>标题三</h3>
        </div>
        <ul id="con">
            <li class="show">内容一</li>
            <li>内容二</li>
            <li>内容三</li>
        </ul>
    </div>

    <script>
        /*
            *选项卡切换
         */
        var oTitle = document.getElementById("title");
        var oCon = document.getElementById("con");
        var oH3s = oTitle.getElementsByTagName("h3");
        var oLis = oCon.getElementsByTagName("li");

        // 分别对三个标题绑定点击事件，让对应的特殊类名给这个元素就可以
        oH3s[2].onclick = function () {
            // 给元素设置类名使用className属性
            // 当点击的时候，先把所有的元素类名都清空，然后点谁给谁设置类名
            oH3s[0].className = ""
            oH3s[1].className = ""
            oH3s[2].className = ""
            oLis[0].className = ""
            oLis[1].className = ""
            oLis[2].className = ""

            oH3s[2].className = "active"
            oLis[2].className = "show"

        }
        oH3s[0].onclick = function () {
            // 给元素设置类名使用className属性

            oH3s[0].className = ""
            oH3s[1].className = ""
            oH3s[2].className = ""
            oLis[0].className = ""
            oLis[1].className = ""
            oLis[2].className = ""

            oH3s[0].className = "active"
            oLis[0].className = "show"

        }
        oH3s[1].onclick = function () {
            // 给元素设置类名使用className属性

            oH3s[0].className = "";
            oH3s[1].className = "";
            oH3s[2].className = "";
            oLis[0].className = "";
            oLis[1].className = "";
            oLis[2].className = "";

            oH3s[1].className = "active";
            oLis[1].className = "show";

        }

    </script>
</body>
</html>
```

###07.进阶版本1
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>选项卡切换页面结构</title>
    <link rel="stylesheet" href="reset.css">
    <style>
        #outer{
            width: 606px;
            margin: 0 auto;
            border: 1px solid #2ba5eb;
        }
        #title{
            overflow: hidden;
        }
        #title>h3{
            width: 200px;
            border: 1px solid #ccc;
            height: 50px;
            text-align: center;
            line-height: 50px;
            color: #333;
            float: left;
        }
        #con{

        }
        #con>li{
            width: 606px;
            height: 300px;
            text-align: center;
            line-height: 300px;
            font-size: 40px;
            font-weight: bold;
            display: none;
        }
        #title>.active{
            background-color: red;
            color: #fff;
        }
        #con>.show{
            display: block;
        }
    </style>

</head>
<body>
    <div id="outer">
        <div id="title">
            <h3 class="active">标题一</h3>
            <h3>标题二</h3>
            <h3>标题三</h3>
        </div>
        <ul id="con">
            <li class="show">内容一</li>
            <li>内容二</li>
            <li>内容三</li>
        </ul>
    </div>

    <script>
        /*
            *选项卡切换
         */
        var oTitle = document.getElementById("title");
        var oCon = document.getElementById("con");
        var oH3s = oTitle.getElementsByTagName("h3");
        var oLis = oCon.getElementsByTagName("li");

        // 分别对三个标题绑定点击事件，让对应的特殊类名给这个元素就可以
        oH3s[2].onclick = function () {
            // 给元素设置类名使用className属性
            //每次点击的时候书写一个for循环，遍历时，判断哪一个和当前点击的对象(this)相等
            // 如果相等则添加类名，否则（不相等）则删除类名
            for (var i = 0; i < oH3s.length; i++) {
                if (oH3s[i] == this){
                    oH3s[i].className = "active";
                    oLis[i].className = "show";
                }else{
                    oH3s[i].className = "";
                    oLis[i].className = "";
                }
            }
        }
        oH3s[0].onclick = function () {
            for (var i = 0; i < oH3s.length; i++) {
                if (oH3s[i] == this){
                    oH3s[i].className = "active";
                    oLis[i].className = "show";
                }else{
                    oH3s[i].className = "";
                    oLis[i].className = "";
                }
            }

        }
        oH3s[1].onclick = function () {
            for (var i = 0; i < oH3s.length; i++) {
                if (oH3s[i] == this){
                    oH3s[i].className = "active";
                    oLis[i].className = "show";
                }else{
                    oH3s[i].className = "";
                    oLis[i].className = "";
                }
            }

        }

    </script>
</body>
</html>
```
###08.进阶版本2
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>选项卡切换页面结构</title>
    <link rel="stylesheet" href="reset.css">
    <style>
        #outer{
            width: 606px;
            margin: 0 auto;
            border: 1px solid #2ba5eb;
        }
        #title{
            overflow: hidden;
        }
        #title>h3{
            width: 200px;
            border: 1px solid #ccc;
            height: 50px;
            text-align: center;
            line-height: 50px;
            color: #333;
            float: left;
        }
        #con{

        }
        #con>li{
            width: 606px;
            height: 300px;
            text-align: center;
            line-height: 300px;
            font-size: 40px;
            font-weight: bold;
            display: none;
        }
        #title>.active{
            background-color: red;
            color: #fff;
        }
        #con>.show{
            display: block;
        }
    </style>

</head>
<body>
    <div id="outer">
        <div id="title">
            <h3 class="active">标题一</h3>
            <h3>标题二</h3>
            <h3>标题三</h3>
        </div>
        <ul id="con">
            <li class="show">内容一</li>
            <li>内容二</li>
            <li>内容三</li>
        </ul>
    </div>

    <script>
        /*
            *选项卡切换
         */
        var oTitle = document.getElementById("title");
        var oCon = document.getElementById("con");
        var oH3s = oTitle.getElementsByTagName("h3");
        var oLis = oCon.getElementsByTagName("li");

        //外层的for循环只是对所有的h3绑定了点击事件  没有其他任何的作用
        for (var i = 0; i < oH3s.length; i++) {
            // 对所有的h3绑定点击事件
            oH3s[i].onclick = function () {
                // 当事件发生的时候，for循环遍历所有的h3，判断当前点击的和哪一个相等，相等的添加类型 否则去掉类名
                for (var i = 0; i < oH3s.length; i++) {
                    if (oH3s[i] == this){
                        oH3s[i].className = "active";
                        oLis[i].className = "show";
                    }else{
                        oH3s[i].className = "";
                        oLis[i].className = "";
                    }
                }
            }
        }


    </script>
</body>
</html>
```
###09.进阶版本3
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>选项卡切换页面结构</title>
    <link rel="stylesheet" href="reset.css">
    <style>
        #outer{
            width: 606px;
            margin: 0 auto;
            border: 1px solid #2ba5eb;
        }
        #title{
            overflow: hidden;
        }
        #title>h3{
            width: 200px;
            border: 1px solid #ccc;
            height: 50px;
            text-align: center;
            line-height: 50px;
            color: #333;
            float: left;
        }
        #con{

        }
        #con>li{
            width: 606px;
            height: 300px;
            text-align: center;
            line-height: 300px;
            font-size: 40px;
            font-weight: bold;
            display: none;
        }
        #title>.active{
            background-color: red;
            color: #fff;
        }
        #con>.show{
            display: block;
        }
    </style>

</head>
<body>
    <div id="outer">
        <div id="title">
            <h3 class="active">标题一</h3>
            <h3>标题二</h3>
            <h3>标题三</h3>
        </div>
        <ul id="con">
            <li class="show">内容一</li>
            <li>内容二</li>
            <li>内容三</li>
        </ul>
    </div>

    <script>
        /*
            *选项卡切换
         */
        var oTitle = document.getElementById("title");
        var oCon = document.getElementById("con");
        var oH3s = oTitle.getElementsByTagName("h3");
        var oLis = oCon.getElementsByTagName("li");

        // js目前没有方法获取一个元素在它父级中的下标
        /*var obj = {};
        obj.name = "lily";//给对象添加一个自定义属性 name 并赋值*/
        // 我自己添加下标
        //     1、元素也是对象，我们可以给元素添加自定义的属性 并设置值
        //     2、给元素扩展自定义对象 保存它的下标
        oH3s[0].a = 0;
        oH3s[1].a = 1;
        oH3s[2].a = 2;

        oH3s[2].onclick = function () {

            for (var i = 0; i < oH3s.length; i++) {
                oH3s[i].className = "";
                oLis[i].className = "";
            }
            this.className = "active";
            // this这个元素是它父级中的下标为几，那么oLis的下标就是几
            oLis[this.a].className = "show";

        }
        oH3s[0].onclick = function () {
            for (var i = 0; i < oH3s.length; i++) {
                oH3s[i].className = "";
                oLis[i].className = "";
            }
            this.className = "active";
            oLis[this.a].className = "show";
        }
        oH3s[1].onclick = function () {
            for (var i = 0; i < oH3s.length; i++) {
                oH3s[i].className = "";
                oLis[i].className = "";
            }
            this.className = "active";
            oLis[this.a].className = "show";
        }


    </script>
</body>
</html>
```
###10.进阶版本4
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>选项卡切换页面结构</title>
    <link rel="stylesheet" href="reset.css">
    <style>
        #outer{
            width: 606px;
            margin: 0 auto;
            border: 1px solid #2ba5eb;
        }
        #title{
            overflow: hidden;
        }
        #title>h3{
            width: 200px;
            border: 1px solid #ccc;
            height: 50px;
            text-align: center;
            line-height: 50px;
            color: #333;
            float: left;
        }
        #con{

        }
        #con>li{
            width: 606px;
            height: 300px;
            text-align: center;
            line-height: 300px;
            font-size: 40px;
            font-weight: bold;
            display: none;
        }
        #title>.active{
            background-color: red;
            color: #fff;
        }
        #con>.show{
            display: block;
        }
    </style>

</head>
<body>
    <div id="outer">
        <div id="title">
            <h3 class="active">标题一</h3>
            <h3>标题二</h3>
            <h3>标题三</h3>
        </div>
        <ul id="con">
            <li class="show">内容一</li>
            <li>内容二</li>
            <li>内容三</li>
        </ul>
    </div>

    <script>
        /*
            *选项卡切换
         */
        var oTitle = document.getElementById("title");
        var oCon = document.getElementById("con");
        var oH3s = oTitle.getElementsByTagName("h3");
        var oLis = oCon.getElementsByTagName("li");

        // js目前没有方法获取一个元素在它父级中的下标
        /*var obj = {};
        obj.name = "lily";//给对象添加一个自定义属性 name 并赋值*/
        // 我自己添加下标
        //     1、元素也是对象，我们可以给元素添加自定义的属性index 并设置值
        //     2、给元素扩展自定义对象 保存它的下标

        /*for (var i = 0; i < oH3s.length; i++) {
            oH3s[i].index = i;
        }*/


        // 外层这个for循环仍然是只绑定点击事件用的
        for (var i = 0; i < oH3s.length; i++) {
            // 这句话借用了 绑定事件的for循环，我们就可以少书写一个for循环
            oH3s[i].index = i;

            oH3s[i].onclick = function () {
                // 里边这个for循环 仅仅是遍历所有的h3和li 然后清空样式
                for (var i = 0; i < oH3s.length; i++) {
                    oH3s[i].className = "";
                    oLis[i].className = "";
                }
                this.className = "active";
                // this这个元素是它父级中的下标为几，那么oLis的下标就是几
                oLis[this.index].className = "show";

            }
        }

       /* oH3s[2].onclick = function () {

            for (var i = 0; i < oH3s.length; i++) {
                oH3s[i].className = "";
                oLis[i].className = "";
            }
            this.className = "active";
            // this这个元素是它父级中的下标为几，那么oLis的下标就是几
            oLis[this.a].className = "show";

        }
        oH3s[0].onclick = function () {
            for (var i = 0; i < oH3s.length; i++) {
                oH3s[i].className = "";
                oLis[i].className = "";
            }
            this.className = "active";
            oLis[this.a].className = "show";
        }
        oH3s[1].onclick = function () {
            for (var i = 0; i < oH3s.length; i++) {
                oH3s[i].className = "";
                oLis[i].className = "";
            }
            this.className = "active";
            oLis[this.a].className = "show";
        }*/

    </script>
</body>
</html>
```
###11.TAB切换i的问题
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>关于tab切换 i的问题</title>
    <link rel="stylesheet" href="reset.css">
    <style>
        #outer{
            width: 606px;
            margin: 0 auto;
            border: 1px solid #2ba5eb;
        }
        #title{
            overflow: hidden;
        }
        #title>h3{
            width: 200px;
            border: 1px solid #ccc;
            height: 50px;
            text-align: center;
            line-height: 50px;
            color: #333;
            float: left;
        }
        #con{

        }
        #con>li{
            width: 606px;
            height: 300px;
            text-align: center;
            line-height: 300px;
            font-size: 40px;
            font-weight: bold;
            display: none;
        }
        #title>.active{
            background-color: red;
            color: #fff;
        }
        #con>.show{
            display: block;
        }
    </style>

</head>
<body>
    <div id="outer">
        <div id="title">
            <h3 class="active">标题一</h3>
            <h3>标题二</h3>
            <h3>标题三</h3>
        </div>
        <ul id="con">
            <li class="show">内容一</li>
            <li>内容二</li>
            <li>内容三</li>
        </ul>
    </div>

    <script>
        /*
            *选项卡切换
         */
        var oTitle = document.getElementById("title");
        var oCon = document.getElementById("con");
        var oH3s = oTitle.getElementsByTagName("h3");
        var oLis = oCon.getElementsByTagName("li");

        /*js代码执行分为同步和异步。
        js优先按照顺序执行同步代码，然后全部同步代码执行完成以后，再去执行异步代码
        当js由上至下执行时碰到异步代码，会让异步代码在旁边排队等待
        异步代码（事件代码，计时器）*/
        for (var i = 0; i < oH3s.length; i++) {
            oH3s[i].index = i;
            oH3s[i].onclick = function () {
                /*for (var i = 0; i < oH3s.length; i++) {
                    oH3s[i].className = "";
                    oLis[i].className = "";
                }*/
                this.className = "active";
                console.log(i);
                // i永远为3  因为执行到这个代码的时候  for循环已经执行完毕 了
                oLis[i].className = "show";

            }
        }


    </script>
</body>
</html>
```

## 九、对象
### 01.什么是对象
- js中,对象是一个设化的概念,任何值都可以转换为对象,以对象的方式进行使用,如数字对象、布尔值对象、字符串对象、类型对象、函数对象、数组对象等,它们都继承 Object类型对象,拥有共同的基本属性和方法。
- 此外, JavaScript也允许自定义对象,从狭义的概念来分析,对象( Object)是最基本的数据类型,是复合型的结构、引用型的数据,它是无序数据集合,对象中每个成员被称为属性

### 02.定义对象
#### 01.构造函数
- 使用new运算符调用构造函数,可以构造一个实例对象,具体用法如下
`var objectName = new functionName (args)`
- 参数说明如下。
>objectName:返回的实例对象
functionName:构造函数,与普通函数基本相同
args:实例对象初始化配置参数列表
```js
    var num1 = new Number(111);
    console.log(num1);

    var obj = new Object({
        name:1
    });
    console.log(obj);
```
#### 02.对象直接量
- 使用直接量可以快速定义对象,也是最高效、最简便的方法
>var objectName = {
属性名1:属性值1,
属性名n:属性值
}
- 在对象直接量中,属性名与属性值之间通过冒号进行分隔,属性值可以是任意类型的数据,属性名可以是 JavaScript标识符,或者是字符串型表达式,属性与属性之间通过逗号进行分隔,最后一个属性末尾不需要逗号。
- 如果属性值是对象,可以设计嵌套结构的对象
- 如果不包含任何属性,则可以定义一个空对象
```js
    var obj1 = {
        name:"lily",
        "sex":"女",
        score:[100,90,80,12,35,34],
        fri:{
            fir1:"xiaowang",
            fir2:"xiaoli",
            fir3:{
                sis1:"dahua",
                sis2:"xiaohua",
                sis3:["zhangdama","zhangxiaoma","zhangma"]
            }
        }
    }
    console.log(obj1.sex);
```
#### 03.使用 Object create
- Object.create是 ECMAScript5新增的一个静态方法,用来定义一个实例对象。
- 该方法可以指定对象的原型和对象特性。具体用法如下`object create (prototype, descriptors)`
- prototype:必须参数,指定原型对象,可以为null
- descriptors可选参数,包含一个或多个属性描述符的 JavaScript对象。属性描述符包含数据特性和访问器特性,其中数据特性说明如下
>value:指定属性值
>writable:默认为 false,设置属性值是否可写
>enumerable:默认为 false,设置属性是否可枚举( for/in)
>onfigurable:默认为flse,设置是否可修改属性特性和删除属性
>访问器特性包含两个方法,简单说明如下set():设置属性值,get():返回属性值
```js
    //3 Object.create方法
    var obj = {};
    console.log(obj);

    var obj2 = Object.create(obj1);
    console.log(obj2);//空对象  但是继承了obj1
    console.log(obj2.name);//自己没有没关系  他爹有


    //创建一个干净的对象
    var obj3 = Object.create(null);
    console.log(obj3);


    //创建一个对象
    var obj4 = Object.create(null,{
        name:{
            value:"xiaowang",
            writable:true,
            enumerable:true,
        },
        sex:{
            value:"nv"
        }
    })
    console.log(obj4);
    console.log(obj4.name);
    obj4.name = "laowang";
    console.log(obj4);

    for(i in obj4){
        console.log(i);
    }


    //访问器属性
    var obj5 = Object.create(null,{
        a:{
            value:"hello",
            writable:true
        },
        b:{
            get:function () {
                return this.a+" world"
            },
            set:function (i) {
                this.a = i + "我拖堂了";
            }
        }
    })
    console.log(obj5);
    console.log(obj5.b);//当调用一个属性的时候，会访问他的访问器属性的get，get方法的返回值就是b的值
    obj5.b = "hahaha";//当设置属性的时候，会调用访问器的set方法，设置的值就是方法的参数
    console.log(obj5);
```

### 03.对象属性的操作
- 属性也称为名值对,包括属性名和属性值。一个对象中不能存在两个同名的属性。属性值可以是任意类型的数据
#### 01.定义属性
##### 01.直接量定义
在对象直接量中,属性名与属性值之间通过冒号分隔,冒号左侧是属性名,右侧是属性值,名值对(属性)之间通过逗号分隔。
```js
    // 01.使用直接量定义
    var obj1 = {
        name:"laowang",
        sex:"男"
    };
    var obj2 = new Object({
        name:"xiaowang",
        sex:"nv"
    })
    var obj3 = Object.create(null,{
        name:{
            value:"dawang",
            writable:true
        },
        sex:{
            value:"nan"
        }
    })

```
##### 02.点语法定义
```js
    // 02.点语法定义：
    var obj4 = {
        name:"xiaozhang"
    }
    obj4.sex = "nan";
    console.log(obj4);

    var obj5 = new Object({
        name:"xiaowang",
        sex:"nv"
    })
    obj5.age = 20;
    console.log(obj5);

    var obj6 = Object.create(null,{
        name:{
            value:"dazhang",
            writable:true,
        }
    })
    obj6.age = 10;//也可以直接对 create创建的对象设置属性，但是无法选择属性的特性，默认可以被修改,可以被枚举
    console.log(obj6);
    obj6.age = 20;
    console.log(obj6);
    for(var i in obj6){
        console.log(i);
    }


```
##### 03.中括号语法
```js
    // 03.中括号语法
    var obj7 = {
        name:"xiaowang"
    }
    var  a= "sex"
    obj7[a] = "nv";
    obj7["sex"] = "nv";
    console.log(obj7);


    function getMess(obj,pro) {
        return obj[pro]
    }
    var myself = {name:"huahua",sex:"nan",age:"19"};
    console.log(getMess(myself, "sex"));


```
##### 04.Object.defineProperty
使用 Object.defineProperty函数可以为对象添加属性,或者修改现有属性。如果指定的属性名在对象中不存在,则执行添加操作:如果在对象中存在同名属性,则执行修改操作
```js
    // 04.Object.defineProperty（obj,pro,{}）
    var obj8 = {
        name:"xiaoli"
    }
    Object.defineProperty(obj8,"sex",{
        value:"nv",
    });
    Object.defineProperty(obj8,"name",{
        //如果修改原有的name属性值，它可以被修改和枚举
        value:"dali",
    });
    console.log(obj8);
    for(var i in obj8){
        console.log(i);
    }
```
##### 05.使用Object.defineProperties
- 可以一次定义多个属性
- Object.defineProperties(object,description)
>object:对其添加或修改属性的对象,可以是本地对象或DOM对象
description:包含一个或多个描述符对象,每个描述符对象描述一个数据属性或访问器属性
```js
    var obj9 = {
        like:"miantiao"
    }
    Object.defineProperties(obj9,{
        color:{
            value:"yellow",
            enumerable:true
        },
        length:{
            value:"10m",
        }
    })
    console.log(obj9);
```
#### 02.读属性
##### 01.使用点语法
使用点语法可以快速读写对象属性,点语法左侧是引用对象的变量,右侧是属性名。
```js
    var obj1 = {
        name:"xiaowang",
        like:"唱跳rap篮球",
        time:"两年半"
    }
    console.log(obj1.name)

```
##### 02.使用中括号语法
- 从结构上分析,对象与数组相似,因此可以使用中括号来读写对象属性
- 在中括号语法中,必须以字符串形式指定属性名,不能使用标识符。
- 中括号内可以使用字符串,也可以使用字符型表达式,即只要表达式的值为字符串即可
```js
// 案例 for in 遍历重写
    var obj1 = {
        name:"xiaowang",
        like:"唱跳rap篮球",
        time:"两年半"
    }

    for(var item in obj1){
        console.log(item);
        obj1[item] = obj1[item] + "@";
    }
    console.log(obj1);
```
##### 02.Object.getOwnPropertyNames
使用 Object.getOwnPropertyNames函数能够返回指定对象私有属性的名称。私有属性是指用户在本
地定义的属性,而不是继承的原型属性。
```js
    var obj1 = {
        name:"xiaowang",
        like:"唱跳rap篮球",
        time:"两年半"
    }
    console.log(Object.getOwnPropertyNames(obj1));//["name","like","time"]
```

##### 03.使用Object.keys
使用 Object.keys()函数仅能获取可枚举的私有属性名称,返回值是一个数组,其中包含对象的可枚举属性名称

##### 04.Object.getOwnPropertyDescriptor()
- 能够获取对象属性的描述符
- Object.getOwnPropertyDescriptor(object,propertyname)
>参数object表示指定的对象，propertyname表示属性的名称，返回值为属性的描述符对象
```js
    //对 create方法创建的对象 进行属性设置
    var obj2 = Object.create(null,{
        name:{
            value:"新宝岛",
            enumerable:true
        },
        time:{
            value:"5min",
            enumerable:true
        },
        like:{
            value:"rap"
        }

    })
    console.log(Object.getOwnPropertyNames(obj2));//["name","like","time"]
    console.log(Object.keys(obj2));//["name","time"]

    console.log(Object.getOwnPropertyDescriptor(obj1, "like"));//{value: "唱跳rap篮球@", writable: true, enumerable: true, configurable: true}
    console.log(Object.getOwnPropertyDescriptor(obj2, "time"));//{value: "5min", writable: false, enumerable: true, configurable: false}

```
#### 03.删除属性
使用 delete运算符可以删除对象的属性
当删除对象属性之后,不是将该属性值设置为 undefined,而是从对象中彻底清除属
```js
    var obj = {
        name:"laowang",
        sex:"nan",
        like:undefined
    }
    console.log(obj.like);//可以设置一个属性值为undefined
    console.log(Object.getOwnPropertyNames(obj));//设置为undefined值的属性名 仍然可以获取到

    delete obj.sex;//删除一个属性
    console.log(obj);
    console.log(Object.getOwnPropertyNames(obj));//当一个属性被删除的话，就枚举不到他的这个属性名了
```

### 04.控制对象状态
- Object.preventExtensions:阻止为对象添加新的属性
- Object.seal:阻止为对象添加新的属性,同时也无法删除旧属性。等价于把属性描述对象的configurable属性设为false。注意,该方法不影响修改某个属性的值
- Object.free:阻止为一个对象添加新属性、删除旧属性、修改属性值
同时提供3个对应的辅助检查函数,简单说明如下:
- Object.isExtensible:检查一个对象是否允许添加新的属性
- Object.isSealed:检查一个对象是否使用了 Object.seal方法
- Object.isFrozen:检查一个对象是否使用了 Object.freeze方法
```js
    // 1.Object.preventExtensions():
    var obj = {
        name:"xiaoxinxin",
        width:"200",
        height:"300"
    }
    console.log(obj);
    obj.color = "red";//设置新属性
    console.log(obj);
    console.log(Object.isExtensible(obj));
    Object.preventExtensions(obj);//阻止设置新属性
    console.log(Object.isExtensible(obj));
    obj.bg = "green";
    console.log(obj);//阻止以后 无法设置新属性


    // 2.Object.seal():
    var obj2 = {
        name:"dadudu",
        width:"200",
        height:"300"
    }
    console.log(obj2);
    delete obj2.width;//删除一个旧属性
    console.log(obj2);
    console.log(Object.isSealed(obj2));
    Object.seal(obj2)//阻止添加新属性 和删除旧属性
    console.log(Object.isSealed(obj2));
    delete obj2.height;
    console.log(obj2);


    // 3.Object.freeze()
    var obj3 = {
        name:"xiaowangba",
        width:"200",
        height:"300"
    }
    console.log(obj3);
    obj3.width = "1000";//修改旧属性
    console.log(obj3);
    console.log(Object.isFrozen(obj3));
    Object.freeze(obj3);
    console.log(Object.isFrozen(obj3));
    obj3.height = "800";
    console.log(obj3);
```

### 05.对象的遍历
```html 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>对象的遍历</title>
</head>
<body>
<script>
    var person = {
        headTeacher:{
            name:"小宁姐",
            sex:"20",
            age:"nv",
            method:"班主任"
        },
        jobTeacher:{
            name:"丽丽",
            sex:"22",
            age:"nv",
            method:"就业"
        },
        bossTeacher:{
            name:"老谭",
            sex:"50",
            age:"男",
            method:"校长"
        }
    }
    console.log(person.length);//undefined 对象是没有length属性的

    function teacherMessage(obj) {
        alert("我的名字是"+obj.name);
        alert("我的年龄是"+obj.age);
        alert("我的性别是"+obj.sex);
        alert("我的作用是"+obj.method);
    }

    // for in 循环  专门用来遍历对象
    // for in中定义的变量 代表着 对象的键名
    for(var i in person){
        // console.log(i);
        teacherMessage(person[i]);
    }
</script>
</body>
</html>
```
### 06.基本类型和引用类型
#### 01.概念
- 数据类型中 分为5种简单的数据类型和1种复杂的数据类型，他们分别对应着基本类型值和引用类型值
- 基本类型值：null  undefined  string  number  boolean
- 引用类型值：object（正则、数组、对象、函数。。。。。）
- 什么这么分类：是按照这两种值存储的方式不同来分类的
#### 02.基本类型值
- 基本类型值：null  undefined  string  number  boolean
- 基本类型值都是按值访问  直接操作保存在变量中的实际值
- 基本类型值都是存储在栈区中，我们可以直接通过变量名访问实际值
```js
    var num1 = 10;//在栈区开启一个空间  栈区的名是变量名  栈区的值是 这个变量所对应的的值
    var num2 = num1; //重新开辟一个区域保存num2的值，获取num1的值 并赋值给num2
    num1 = 30;//改变栈区num1的值为30   但是不会影响num2
    console.log(num1,num2);//30 10
```
- 基本类型值的特点：
>1、基本类型的值是不可变的
2、我们不能给基本类型值添加属性和方法  就算添加也是获取不到的
3、基本类型的比较是值的比较
4、基本类型的变量是存放在栈区的（栈区指内存里的栈内存),栈区包括了变量的标识符和变量的值
```js
    // 1、基本类型的值是不可变的
        /*数组添加一个值，还是原来的数组。
        如果基本类型值发生改变，那么久不再是原来的值，而是重新赋值了。
        所以我们不能改变基本类型的值，否则就是直接换了值*/

    // 2、我们不能给基本类型值添加属性和方法  就算添加也是获取不到的
    var str1 = "abc";
    str1.eat = "apple";//给基本类型 扩展了一个属性  eat
    str1.say = function () {//给基本类型值 扩展一个方法
        alert("你说话呀");
    }
    console.log(str1.eat);//undefined
    str1.say();//str1.say is not a function


    // 3、基本类型的比较是值的比较
    var num1 = 5;
    var num2 = null;
    console.log(num1 < num2);//基本类型值的比较 都是拿出变量所对应的值来进行比较的  先取出来再转换类型比较

    // 4、基本类型的变量是存放在栈区的（栈区指内存里的栈内存),栈区包括了变量的标识符和变量的值


```
#### 03.引用类型值
- 引用类型值再栈区储存的是 标识符（变量名）和引用地址   在堆区储存的是对象的值
- 当我们访问某一个对象的时候，要先访问到栈区的地址 然后引用到堆区的值
```js
    var obj1 = {
        name:"lily"
    }//声明一个对象，然后值保存在堆区  变量和引用地址保存在栈区
    var obj2 = obj1;//赋值都是 栈区引用地址的赋值  把obj1的地址赋值给了obj2
    obj1.name = "lucy";//改变了obj1 堆区对象值的内容
    console.log(obj1,obj2);//obj1 和obj2 引用地址是一样的 所以指向的是同一个对象
```

- 引用类型值特点：
>1、引用类型的值是可变的，我们可以为引用类型添加属性和方法
2、引用类型的值是同时保存在栈内存和堆内存中的对象
3、引用类型的比较是引用的比较
```js
// 1、引用类型的值是可变的，我们可以为引用类型添加属性和方法
    var arr1 = [1,2,3];
    arr1.say = function () {
        alert("你好呀");
    }
    arr1.say();

    // 2、引用类型的值是同时保存在栈内存和堆内存中的对象

    //3、引用类型的比较是引用的比较
    var obj1 = {};
    var obj2 = {};
    console.log(({} == {}));//false  两个对象虽然是空对象  然后再栈区的地址不一样  而比较是栈区的引用地址的比较  所以返回false

```

## 十、数组
### 01.什么是数组
- 数组(Array)是有序数据集合,数组中的每个成员被称为元素(Element),每个元素的名称(键)被称为数组下标(index),数组内不同元素的值可以为不同类型,数组的长度是弹性的、可读写的,在Javascript脚本中数组主要用于临时寄存同类数据,进行高速批量运算。
```js
    var arr = [123,"abc",null,undefined,{name:"xioawang"},true,[1,2,3],function () {
        alert(1);
    }];
    console.log(arr);
    // arr[arr.length - 1]();
    arr.length = 100;
    console.log(arr);
```
### 02.定义数组和读写数组
#### 01.构造数组
- 使用new运算符调用Array()类型函数时,可以构造一个新数组
- 直接调用Array函数,不传递参数,可以创建一个空数组
- 传递多个值，可以创建一个实数组
- 传递一个数值参数,可以定义数组的长度,即包含元素的个数，参数值等于数组的length属性值,每个元素的值默认值为 undefined
- 使用中括号可以读写数组，中括号左侧是数组名称，中括号内为数组下标
```js
    // 1.构造数组：
    var arr1 = new Array();//如果不传值，则构造一个空数组
    console.log(arr1);

    var arr2 = new Array("a","b",23,45);
    console.log(arr2);

    var arr3 = new Array(4);
    console.log(arr3);//如果传递一个参数，是定义数组的长度

    var arr4 = new Array("a");
    console.log(arr4);

    console.log(arr2[2]);//读取数组的值
```
#### 02.数组直接量
- 数组直接量的语法格式:在中括号中包含多个值列表,值之间用号分隔（推荐使用数组直接量定文d 数组,因为数组直接量是定义数组最简便、最高效的方法）
```js
    var arr5 = [1,2,3,4,5];//直接量定义数组
    console.log(arr5);
    console.log(arr5[3]);//读取数组
```
#### 03.多维数组
- Javascript不支持多维数组,设置元素的值等于数组,可以模拟二维数组结构,如果三维组中每个元素的值也为数组,则可以模拟三维数组,以此类推,通过数组套的形式可以定义多推数组
- 读写多维数组方法与普通方法相同，都是使用中括号进行访问
```js
    var arr6 = [1,2,3,[4,5,6],7];//定义一个二维数组
    console.log(arr6);
    console.log(arr6[3][1]);//二维数组的获取值
    var arr7 = [1,2,3,4,5,[5,6,7,[8,9],11],10];//定义一个三维数组
    console.log(arr7);
    console.log(arr7[5][3][1]);//三维数组的获取



    //使用for 把1-100的整数以二维的形式储存在数组中
    var arr8 = [];
    // 遍历10次，每次生成一个10个值的数组
    for (var i = 0; i < 10; i++) {
        // 创建一个新数组，每次遍历的时候，插入10个值，然后把这个数组，插入到arr8中
        var arr9 = [];
        //遍历10次，每次向arr9中插入1个值
        for (var j = 0; j < 10; j++) {
            arr9[j] = i * 10 + j + 1;
        }
        arr8[i] = arr9;
    }
    console.log(arr8);
```
#### 04.空位数组
- 空位数组就是数组中包含空元素。所谓空元素,就是在语法上数组中两个逗号之间没有任何值。出现空位数组的情况如下
>1)直接量定义
2)构造函数定义
3）delete删除
- 空元素可以读写, length属性不排斥空位,如果使用for语句和 length属性遍历数组,空元素都可以
被读取,空元素返回值为undefined
```js
    var arr10 = [1,2,,4];//空位数组，找不到，所以空位的值返回undefined
    var arr11 = [1,2,undefined,4];//有值，值为undefined
    console.log(arr10);
    console.log(arr11);
```

#### 05.关联数组
- 如果数组的下标值超出范围,如负数、浮点数、布尔值、对象或其他值，js会自动把它转换为一个字符串,并定义为关联数组。
- 关联数组就是与数组关联的对象,简单地说就是数组对象,字符串下标就是数组对象的属性
```js
    var arr12 = [1,2];
    arr12[3.1] = "haha";//相当于给数组扩展了一些属性和方法
    arr12[true] = "buer";
    console.log(arr12);
    console.log(arr12[3.1]);
```

#### 06.伪类数组
- 伪类数组,也称为类数组,即类似数组结构的对象。简单地说,就是对象的属性名为非负整数,且从0开始,有序递增,同时包含length属性,还应确保其值与有序下标属性个数保持动态一致,以方便对伪类数组进行选代操作。
- 由于数字数非法标识符，所以需要用点来读写属性
```js
    var obj1 = {
        0:"a",
        1:"2",
        2:"c",
        3:"d",
        length:4
    }
    console.log(obj1[1]);
```

#### 07.斐波那契数列
```js
    //打印出斐波那契数列的前100个值 在数组中
    // 1,2,3,5,8,13 初始值1和2   其他的值是前两个值的和
    // arr[6] = arr[4]+arr[5]
    var arr = [1,2];
    for (var i = 2; i < 100; i++) {
        arr[i] = arr[i-2] + arr[i-1];
    }
    console.log(arr);


```

### 03.数组的长度
- 每个数组都有一个length属性，该属性返回数组的最大长度。
- length属性可读可写，是一个动态属性。
- length属性值也会随数组元素的变化而自动更新。同时如果重置了length属性值，也将影响数组的元素。
```js
    var arr1 = [];
    arr1.length = 100;
    console.log(arr1);//empty*100
    console.log(arr1[10]);//undefined

    var arr2 = [1,2,3];
    arr2.length = 5;
    console.log(arr2);

    var arr3 = [1,2,3,4,5,6,7];
    arr3.length = 2;
    console.log(arr3);//[1,2]
```

### 04.操作数组
#### 01.栈操作
- 使用push()和pop()方法,可以在数组的尾部执行操作。
- 其中push方法，能够把一个或多个参数附加到数组的尾部，并返回附加元素以后，数组的长度
- pop方法是能够删除数组中的最后一个元素，并返回删除的值
补充：栈是先进后出，后进先出的原则。类似的情况是，叠放物品，或者子弹上膛
```js
    var arr = [];//空栈
    console.log(arr.push(1));//入栈 返回新长度
    console.log(arr.push(2,3));//入栈 一次可以插入多个值 返回新长度
    console.log(arr);

    console.log(arr.pop());//出栈 返回删除的值
    console.log(arr.pop());//出栈 返回删除的值
    console.log(arr);
```
- 栈操作练习
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>栈操作练习 -进制转换</title>
</head>
<body>
<script>
    function to2b(num) {
        var arr = [];//一个新栈，把每次生成的余数压到栈里
        var r = null;//用来保存每次生成的余数
        var s = "";//最后返回的二进制字符串
        while(num > 0){
            r = num % 2;//求出每次的余数
            arr.push(r);//把余数入栈
            num = parseInt(num / 2);//求出num计算后的值 并向下取整
        }
        while(arr.length > 0){
            s += arr.pop();//pop是把最后一个值删了 并返回出来 和s拼接  放在了s的首位
        }
        return s;
    }

    console.log(to2b(100));
    console.log(to2b(1000));
    console.log(to2b(3));
    // console.log((100).toString(2));//1100100
</script>
</body>
</html>
```

- 栈数据结构方法封装
```js
var arr = [3,5,2,3,6,1,6];
    // push:添加一个新元素到栈顶
    function push(arr) {
        // arguments
        for (var i = 1; i < arguments.length; i++) {
            arr.push(arguments[i]);
        }

    }
    push(arr,1,2,3)
    // pop方法 移出栈顶的元素  并且得到移出的值
    function pop(arr) {
        return arr.pop();
    }

    // peek:返回栈顶元素 不对栈做修改
    function peek(arr) {
        return arr[arr.length - 1]
    }

    // console.log(peek(arr));

    // isEmpty 判断栈中是否为空  如果为空则返回true 否则返回false
    function isEmpty(arr) {
        return arr.length == 0
    }

    // clear:清空整个栈
    function clear(arr) {
        arr.length = 0;
    }

    // size:返回栈里的个数
    function size(arr) {
        return arr.length;
    }
```

- 栈结构练习-可定制的进制转换
```js
    //封装一个栈操作的一个类  想要使用 直接new 实例化
    //实例化得到的对象 就会拥有这些方法
    function Stack() {
        this.arr = [];
        this.push = function (item) {
            this.arr.push(item);
        };
        this.pop = function () {
            return this.arr.pop();
        };
        this.peek = function () {
            return this.arr[this.arr.length - 1];
        };
        this.isEmpty =function () {
            return this.arr.length == 0;
        };
        this.clear = function () {
            this.arr = [];
        };
        this.size = function () {
            return this.arr.length;
        };
    }

    // 16进制以下所有进制转换算法
    function divideBy2(num,para) {
        //把Stack实例化以后  所有的remStack就会拥有Stack这个类的属性和方法
        var remStack = new Stack();
        var rem;
        var binarySting = "";
        var str = "0123456789abcdef";
        //循环插入栈
        while(num>0){
            rem = parseInt(num % para);
            remStack.push(rem);
            num = parseInt(num / para);
        }
        // 当全部插入完成以后，对栈进行一个移出的操作
        while(!remStack.isEmpty()){

            binarySting += str[remStack.pop()];
        }
        return binarySting;
    }

    console.log(divideBy2(2821355,12));
    console.log(divideBy2(4,16));
```
#### 02.队列操作
- 使用unshift()和 shift()方法可以在数组头部执行操作
- 其中unshift()能够把一个或多个参数值附加到数组的头部,第1个参数为数组新的元素0,第2个参数为新的元素1,以此类推,最后返回添加元素后的数组长度
- shift方法能够删除数组第1s个元素,并返回该元素,然后将余下所有元素前移1位,以填补数组头部的空缺。如果数组为空, shift将不进行任何操作,返回 undefined
- 使用 unshift分批插入元素与一次性插入元素结果是不同的
- 将pop()与 unshift()方法结合,或者将 push()与 shift()方法结合使用,可以模拟队列
```js
// 利用队列模式把数组元素的所有值放大10倍
var a = [1,2,3,4,5];
for(var i in a){
    var t = a.pop();
    a.unshift(t*10);
}
console.log(a);
```
- 补充：队列也是一种运算受限的线性表,不过与枝操作不同,队列只允许在一端进行插入操作,在另一端进行删除操作。队列通循先进先出、后进后出的原则,类似的行为在生活中比较常见,如排队购物、任务排序等。在 Javascript动画设计中,也会用到队列操作来设计回调函数。
```js
// 猴子找大王游戏
// 有一群猴子排成一圈,按1、2、3、…、n依次编号，然后从第1只开始数,数到第m只,则把它踢出圈,然后从它后面再开始数,当再次数到第m只,继续把它踢出去,以此类推,直到只剩下一只猴子为止,那只猴子就叫作大王。要求编程模拟此过程,输入m和n，输出最后那个大王的编号
// n表示猴子个数，m表示踢出位置
function f(n,m){
    //将猴子编号并放入数组
    var arr = [];
    for(var i = 1;i < n+1;i++){
        arr.push(i);
    }
    //当数组内只剩下一只猴子的时候跳出循环
    while(arr.lenght>1){
        //定义排队轮转次数
        for(var i = 0;i<m-1;i++){
            //队列操作完成轮转
            arr.push(arr.shisft());
        }
        arr.shift();//提出第m只猴子
    }
    return arr;
}

```

- 队列结构的封装
```js
/*enqueue：向队列的尾部添加新的项
    dequeue：移除队列的第一个项，并返回被移除的元素
    front：返回队列的第一个元素，队列不做任何的改动
    isEmpty：如果队列中不包含任何元素，返回true，则返回true，否则返回false
    size:返回队列包含的元素个数*/

    function Queue() {
        this.arr = [];
        this.enqueue = function (item) {
            this.arr.push(item)
        }
        this.dequeue = function () {
            this.arr.shift();
        }
        this.front = function () {
            return this.arr[0];
        }
        this.isEmpty = function () {
            // return this.arr.length == 0;
            return !this.arr.length;
        }
        this.size = function () {
            return this.arr.length;
        }
    }

    var queue1 = new Queue();
```


#### 03.删除元素
- 使用pop方法可以删除尾部的元素,使用shift方法可以删除头部的元素
- 使用delete运算符能删除指定下标位置的数组元素,删除后的元素为空位元素,删除数组length保持不变
- 使用length属性可以删除尾部一个或多个元素,甚至可以清空整个数组
- 使用splice方法可以删除指定下标位置后一个或多个数组元素（个数）
```js
    // 使用delete删除指定下标的元素
    var arr1 = [1,2,3,4,5];
    delete arr1[2];//删除指定下标的值，当前的值为空，所以数组变成了空位数组 长度不变
    console.log(arr1);

    // 使用length属性也可以删除数组
    var arr2 = [1,2,3,4];
    arr2.length = 1;
    console.log(arr2);


    var arr3  = [1,2,3,4,5,5,6,7,8,8];
    console.log(arr3.splice(3));//一个参数代表删到末尾
    console.log(arr3);//[1,2,3]

    var arr4  = [1,2,3,4,5,5,6,7,8,8];
    console.log(arr4.splice(3,3));//两个个参数代表删几个 [4,5,5]
    console.log(arr4);//[1,2,3,6,7,8,8]
```

#### 04.添加元素
- 使用 push方法可以在尾部添加一个或多个元素,使用 unshift方法可以在头部附加一个或多个元素
- 通过中括号和下标值,可以为数组指定下标位置添加新元法来添加元素
- concat方法能够把传递的所有参数按顺序添加到数组的尾部
    >  - concat方法可以跟随多个参数,并把它们作为元素按顺序连接到数组的尾部
    >- 如果参数是数组,则concat方法会把它打散,分别作为单独的元素连接到数组的尾部
    >- 不过concat方法仅能够打散一维数组,它不会打散二维的数组。
    >- concat方法将创建并返回一个新数组,而不是在原来数组基础上添加新元素。所以,如果要在原数组着础上添加元素,建议使用 push方法和unshift方法来实现。但是 push方法和 unshift方法不能够打散参数数组，而是把它作为单独的参数执行添加操作
- 使用 splice方法在指定下标位置后添加一个或多个元素
```js
    // 可以使用中括号和下标值 来添加元素，或者是修改元素
    var arr1 = [1,2,3,4,5];
    arr1[5] = 6;
    arr1[10] = 10;//如果给后边元素设置值，中间的空白就变成了空位元素
    arr1[1] = "a";//这种方法只能给空位元素设置，或者是其他的没有的位置设置，否则就修改了元素
    console.log(arr1);


    // concat方法
    var arr2 = ["a","b","c"];
    console.log(arr2.concat(1, 2, 3));;
    console.log(arr2);//原数组不改变


    var arr2 = ["a","b","c"];
    arr2.push([1,2,3]);//push插入会把数组直接当成1个值插入
    console.log(arr2);

    var arr2 = ["a","b","c"];
    console.log(arr2.concat([1, 2, 3,[4,4,4]]));


    // splice方法可以在指定位置的下标添加元素
    var arr3 = ["a","b","c","d","e","f"];
    arr3.splice(2,0,"g","h");//无论是否删除，都会把第三个参数以后的所有参数 按顺序放在第一个参数下标标记的位置
    console.log(arr3);
```

#### 05.使用 splice()方法
- splice()方法的参数都是可选的。如果不给它传递参数,则该方法不执行任何操作
- 如果给它传递一个数,则该方法仅执行删除操作,参数值指定删除元素的起始下标(包括该下标元素),splice方法将删除后面所有
- 如果指定两个参数,则第2个参数值表示要别删除元素的个数。
- 如果指定三个或多个参数,则第3个以及后面所有参数都被视为插入的元素
- 如果不执行删除操作,第2个参数值应该设置为0,但是不能够空缺,否则该方法无效
- splice方法执行的返回值是被别除的子数组
- 当第1个参数值大于length属性值时,被视为在数组尾部执行操作,因此删除无效,但是可以在尾部插入多个指定元素
- 参数取负值问题。如果第1个参数为负值,则按绝对值从数组右侧开始向左侧定位。如果第2个参数为负值,则被视为0。
```js
    var arr1 = [1,2,3,4,5,6,7];
    console.log(arr1.splice(4));//[5,6,7]
    console.log(arr1);//[1,2,3,4]


    var arr2 = [1,2,3,4,5,6,7];
    console.log(arr2.splice(1,3));//[2,3,4]
    console.log(arr1);//[1,5,6,7]

    var arr3 = [1,2,3,4,5,6,7];
    console.log(arr3.splice(2,1,"a","b","c"));//[3]
    console.log(arr3);//[1,2,a,b,c,4,5,6,7]

    var arr4 = [1,2,3,4,5,6,7];
    console.log(arr4.splice(10,2,"a","b","c"));//[]
    console.log(arr4);//[1,2,3,4,5,6,7,a,b,c]

    var arr5 = [1,2,3,4,5,6,7];
    console.log(arr5.splice(-5,2,"a","b","c"));//[3,4]
    console.log(arr5);//[1,2,a,b,c,5,6,7]

    var arr5 = [1,2,3,4,5,6,7];
    console.log(arr5.splice(-5,-2,"a","b","c"));//[]
    console.log(arr5);//[1,2,a,b,c,3,4,5,6,7]
```

#### 06.使用slice()方法
- slice方法与splice方法功能相近,但是它仅能够截取数组中指定区段的元素,并返回这个子数组
- 该方法包含两个参数,分别指定截取子数组的起始和结束位置的下标
- 第1个参数指定起始下标位置,包括该值指定的元素;第2个参数指定结束位置,不包括指定的元素。
- 该方法的参数可以自由设置。如果不传递参数,则不会执行任何操作:如果仅指定一个参数,则表示从该参数值指定的下标位置开始,截取到数组的尾部所有元素
- 当参数为负值时,表示按从右到左的顺序进行定位,即倒数定位法,而不再按正数顺序定位(从左到右),但取值顺序依然是从左到右,如果起始下标值大于或等于结束下标值,将不执行任何操作
- sliced方法将返回数组的一部分(子数组),但不会修改原数组
```js
    var arr1 = [1,2,3,4,5,6,7,8];
    console.log(arr1.slice(3));//[4,5,6,7,8]
    console.log(arr1);

    var arr1 = [1,2,3,4,5,6,7,8];
    console.log(arr1.slice(3,6));//[4,5,6]
    console.log(arr1);

    var arr1 = [1,2,3,4,5,6,7,8];
    console.log(arr1.slice(-3,6));//[6]
    console.log(arr1.slice(-6,5));//[3,4,5]
```
#### 07.数组排序-reverse方法
- reverse方法能够颠倒数组元素的排列顺序，该方法不需要参数
- 改变原来数组，不创建新数组
```js
    var arr = [1,2,"a","2","b",1,[1]];
    console.log(arr.reverse());
    console.log(arr);


    // 手写reverse反转
    function reverse(arr) {
        var newArr = [];
        for(var i in arr){
            newArr.unshift(arr[i]);
        }
        return newArr;
    }
    console.log(reverse([1, 4, 3, 2, 5, 1]));
```

#### 08.数组排序 - sort方法
- sort方法能够根据一定条件对数组元素进行排序。如果调用sort方法时没有传递参数,则按字母顺序对数组中的元素进行排序。
- sort方法可以根据其他顺序执行操作。这时就必须为方法提供一个函数参数,该函数要比较两个值,然后返回一个用于说明这两个值的相对顺序的数字
```js
    var arr = [1,2,3,4,22,34,32,34,100];
    console.log(arr.sort());
    console.log(arr);

    var arr = [1,2,4,3,22,34,32,34,100];
    /*arr.sort(function (a,b) {
        console.log(a,b)
        //sort每次传入两个值，第一个参数a是后边的值，第二个参数b是前边的值
        //如果返回的正数，则两个值不交换位置，如果返回的是负数，则两个值交换位置
        if (a > b){
            return 1;
        }else if(a < b){
            return -1;
        }else{
            return 0;
        }
    });*/
    arr.sort(function (a,b) {
        return a - b;//升序排列
    })
    console.log(arr);


    var arr = [1,2,4,3,22,34,32,34,100];
    /*arr.sort(function (a,b) {
        if (a > b){
            return -1;
        }else if(a < b){
            return 1;
        }else{
            return 0;
        }
    });*/

    arr.sort(function(a,b){
        // return -(a - b);//降序
        return b - a;
    })
    console.log(arr);
```

```js
    // 对对象进行排序：
    var persons = [
        {name:"lily1",sex:"女",age:18},
        {name:"lily2",sex:"女",age:19},
        {name:"lily3",sex:"女",age:11},
        {name:"lily4",sex:"女",age:28},
        {name:"lily5",sex:"女",age:22},
        ]
    
    //请对数组persons进行按照年龄升序排序
    persons.sort(function (a,b) {
        if (a.age>b.age) {
            return 1;
        }else if(a.age<b.age){
            return -1;
        }else{
            return 0;
        }
    })
    console.log(persons);
```

```html
<!-- 动态加载数据，及对象数据排序 -->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
<button id="price">价格排序</button>
<button id="hot">热度排序</button>
<button id="num">销量排序</button>
<ul id="list">
    <li class="outer">
        <h2>苹果手机</h2>
        <p>销量：<span>10000</span></p>
        <p>价格：<span>11988</span></p>
        <p>热度：<span>299</span></p>
    </li>
    <li>
        <h2>苹果手机</h2>
        <p>销量：<span>10000</span></p>
        <p>价格：<span>11988</span></p>
        <p>热度：<span>299</span></p>
    </li>
    <li>
        <h2>苹果手机</h2>
        <p>销量：<span>10000</span></p>
        <p>价格：<span>11988</span></p>
        <p>热度：<span>299</span></p>
    </li>
</ul>
<script>
    var oList = document.getElementById("list");
    var oPrice = document.getElementById("price");
    var oHot = document.getElementById("hot");
    var oNum = document.getElementById("num");
    var data ={
        phone:[
            {brand:"苹果手机",num:"10000",price:"11988",hot:"199"},
            {brand:"联想手机",num:"9000",price:"1988",hot:"1199"},
            {brand:"华为手机",num:"20000",price:"12988",hot:"1299"},
            {brand:"三星手机",num:"13000",price:"7988",hot:"3199"},
            {brand:"魅族手机",num:"4000",price:"988",hot:"1099"},
            {brand:"小米手机",num:"14000",price:"19988",hot:"109"},
            {brand:"锤子手机",num:"100",price:"88",hot:"199999"},
        ],
        img:[
            "01.jpg","02.jpg","03.jpg"
        ]
    }
    var phoneDate = data.phone;
    showPhone(phoneDate);
    function showPhone(data) {
        oList.innerHTML = "";
        for(var i in data){
            var str = `
                <li>
                    <h2>${data[i].brand}</h2>
                    <p>销量：<span>${data[i].num}</span></p>
                    <p>价格：<span>${data[i].price}</span></p>
                    <p>热度：<span>${data[i].hot}</span></p>
                </li>
            `;
            oList.innerHTML += str;
        }
    }

    // 点击价格降序
    oPrice.onclick = function () {
        phoneDate.sort(function (a,b) {
            if (+a.price > +b.price){
                return -1;
            }else{
                return 1;
            }
        })
        //当数据发生变化以后，再次调用字符串拼接函数，重新向页面赋值
        showPhone(phoneDate);

    }

    // 点击热度降序
    oHot.onclick = function () {
        phoneDate.sort(function (a,b) {
            if (+a.hot > +b.hot){
                return -1;
            }else{
                return 1;
            }
        })
        //当数据发生变化以后，再次调用字符串拼接函数，重新向页面赋值
        showPhone(phoneDate);

    }

    // 点击热度降序
    oNum.onclick = function () {
        phoneDate.sort(function (a,b) {
            if (+a.num > +b.num){
                return -1;
            }else{
                return 1;
            }
        })
        //当数据发生变化以后，再次调用字符串拼接函数，重新向页面赋值
        showPhone(phoneDate);

    }

</script>
</body>
</html>
```

#### 09.数组转换 - toString()
- 数组中 toString把每一个元素转为字符串，然后是使用逗号连接z输出显示。
- 当数组用于字符串环境中时，JS会自动调用toString()方法把数组转为字符串。
```js
    var arr = [1,2,"a",null,{name:"lily"}];//null和undefined没有toString方法
    console.log(arr.toString());//1,2,a,,[object Object]

    //改写Array的toString方法
    Array.prototype.toString = function () {
        alert(1);
        return "没有返回值 哈哈哈"
    }
    var arr = [1,2,3];
    console.log(arr + "1");
    // console.log(arr);


    
```

#### 10.数组转换 - toLocalString()
- toLocalString方法和toString方法相同，主要区别在于toLocalString方法能够使用户所在地区特定的分隔符把生成的字符串连接起来。
- 根据中国习惯，先把数字转为浮点数之后，再执行字符串
```js
    var arr = ["1.00",222222,3,4,"a"];
    console.log(arr.toLocaleString());
    console.log(arr.toString());
```

#### 10.数组转换 - join()
- join方法可以把数组转换为字符串,不过它可以指定分隔符,在调用join方法时,可以传递一个参数作为分隔符来连接每个元素,如果省略参数,默认使用逗号作为分隔符,这时与toString方法转换操作效果相同。
- 返回一个转换后的字符串，并没有改变原数组
- 如果不想要间隔 可以输入一个空字符串
- 如果数组的值是其他类型 在数组中 如果遇到null或者undefined 直接转换成空字符串  其他按照toString规则转换
```js
    var arr = ['1',2,'c',4,5,null];
    console.log(arr.join());//返回字符串
    console.log(arr);

    console.log(arr.join("-"));//返回字符串
    console.log(arr.join(""));//返回字符串
```

#### 11.元素定位 - indexOf和lastIndexOf
- 使用indexOf和lastIndexOf方法可以检索数组元素,返回指定元素的索引位置
- indexof返回某个元素值在数组中的第1个匹配项的索引,如zaz果没有找到指定的值,则返回-1.
- 第二个参数可选，表示开始搜索的数组索引。如果省略，则从索引0处开始搜索
- lastIndexOf返回指定的值在数组中的最后一个匹配项的索引，用法和indexOf相同
```js
    var arr = ["xiaowang","xiaoli","xiaozhang","xiaoqian","xiaomao","xiaozhang","xiaozhang2"];
    var userStr = "xiaozhang";
    var userStr2 = "maoge";
    console.log(arr.indexOf(userStr,3));
    console.log(arr.indexOf(userStr));
    console.log(arr.indexOf(userStr,6));
    console.log(arr.indexOf(userStr2));


    console.log(arr.lastIndexOf("xiaozhang",2));//第二个参数是限制某一个范围，返回的仍然是下标
```

#### 12.检测数组
- isArray是Array类型的一个静态方法,使用它可以判断一个值是否为数组。
- 使用 Array.isArray();z
- typeOf运算符只能显示数组的类型是Object,而 Array.isArray方法可以直接返回布尔值。在条件表达式中,使用该方法非常实用.
- 使用in运算符可以检测某个值是否存在于数组中,注意,in运算符主要用于对象,但也适用于数组
```js
    var  a = "123";
    var b = [6,2,3,4];
    console.log(Array.isArray(a));//false
    console.log(Array.isArray(b));//true
    console.log(6 in b);//false


    var obj = {
        name:"xiaowang",
        sex:"nan"
    }
    console.log('name' in obj);
```

#### 13.检测是否全部符合-every方法
- every方法可以测试的所有元素是否都满足指定的测试
- every中是函数，每一项数组的值，依次进入函数运行，函数最终要要求返回布尔值。
- 如果有一项返回false，则停止执行，every返回false
- 如果所有的项全部返回true  那么 整个every方法就返回true
- every方法的函数拥有3个参数：1、item  数组的每一项 2、index  数组的这一项 对应的下标  3、array  原数组
- every方法还有第二个可选的参数，可在回掉函数中为其引用this关键字的对象。如果省略，则undefined是this值
```js
// 我们得到一组年龄,如果所有的人都成年了，那么我们就开启成人网吧模式,否则 就进入儿童模式
    var userAges = [18,19,19,19,22,29,50,80,45];
    var isPerson = userAges.every(function (item,index,array) {
        console.log(item,index,array);
        var re = true;
        if (item < 18){
            re = false;
        }
        return re;
    });
    if (isPerson){
        alert("进入成人模式  坐稳了")
    }else{
        alert("儿童模式")
    }

    // 可以简单点：
    var isPerson = userAges.every(function (item,index,array) {
        return item >= 18;
    });
    if (isPerson){
        alert("进入成人模式  坐稳了")
    }else{
        alert("儿童模式")
    }


    // 检测数组中的数是否都是偶数
    var arr = [1,2,3,4];
    var isEven = arr.some(function(item,index,arr){
        if(item % 2 == 0){
            return true;
        }else{
            return false
        }
    })
    if(isEven){
        console.log("偶数")
    }else{
        console.log("不全是偶数")
    }


    //检测数组中元素的值是否有在指定的范围内，返回值用一个对象设置
    var obj = {max:20,min:10};
    var arr = [12,13,19];
    var isScope = arr.some(function(item){
        if(typeof item !== "number"){
            return false
        }else{
            return item>=this.min && item <=this.max
        }

    },obj)
```

#### 14.检测是否存在符合 - some方法
- 使用some方法可以确定数组的元素是否有满足指定的测试的项
- 只要一项返回true  那么 some方法就返回true（一真即真）
- 其余和every类似
```js
    // 我们得到一组年龄,如果所有的人都成年了，那么我们就开启成人网吧模式,否则 就进入儿童模式
    var userAge = [19,18,21,23,14,45];
    var isPerson = userAge.some(function (item,index,array) {
        return item < 18;
    });
    if (isPerson){
        alert("儿童模式")
    } else{
        alert("成人模式")
    }


    //this指向对象的
    var arr = [18,19,20,21,30,11,14,19,40];
    var isTrue = arr.some(function (item,index,array) {
        // return item < 18;
        return item < this.max;
    },{max:18})
    console.log(isTrue);
```

#### 15.for迭代数组
- for和for/in语句都可以迭代数组，for语句需要配合length属性和数组的下标实现。执行效率没有for/in高。
- for/in 也会跳过空元素
```js
    var arr = ["a","b","c",,"e"];
    for (var i = 0; i < arr.length; i++) {
        console.log(arr[i]);//a b c undefined e
    }

    for(var j in arr){
        console.log(j,arr[j]);//a b c e
    }
```
#### 16.forEach
- Array类型为每一个数组定义了forEach方法，可以对数组进行迭代操作
- forEach中一个迭代函数，一个可选的this引用的对象
- 不会对空元素调用回掉函数
- foreach方法 用来遍历数组的每一项  forEach方法没有返回值
```js
// 使用forEach迭代数组，计算数组元素的和

    //一个家庭的年龄 过年了  每个人长1岁
    //方法1 创建一个新数组
    var userAages = [19,21,18,34,32,25,45];
    var newUserAges = [];
    userAages.forEach(function (item,index,array) {
        newUserAges[index] = item + 1;
    })
    console.log(newUserAges);
    //方法2 直接改变原来数组
    var re = userAages.forEach(function (item,index,array) {
        userAages[index] = item + 1;
    })
    console.log(userAages);
    console.log(re);
```

#### 17.使用keys迭代
- keys()是Object的静态函数,专门用来遍历对象获取键名, Object.keys函数的参数是一个对象,返回一个数组,元素是该对象所有本地属性名。
如果使用该函数选代数组,可以汇集数组的所有元素下标值。
- 除了获取键名集合外,使用keys还可以间接统计对象的长度
- Object还有一个类似的静态函数: getOwnPropertyNames,与keys用法相同,参数都是对象,返回值都是数组,数组元素都是属性名。不同点:keys仅能选代本地、可枚举的属性, getownPropertyNames可以迭代所有
```js
    var arr = ["a","b","c",,"d"];
    console.log(Object.keys(arr));;
```
#### 18.映射数组
- 使用map方法可以对数组的每一个元素调用指定的回调函数，并返回包含结果的数组。
- arr.map(function(){},thisArg)
- map方法返回一个新数组，其中每一个元素均为关联的原始数组元素的回调函数返回值。
- map不会为缺失的元素调用回调函数
```js
    //把数组中的每个元素的值平方，乘以PI的值，把返回的圆的面积作为新数组的元素值，最后返回这个新数组

    // 有一个数组装着2019年所有人的年龄，2020年以后，每个人的年龄都增加1岁
    var allAge = [19,15,,2,30,32,43,45];
    var age2020 = allAge.map(function (item,index,arr) {
        return item+1;
    })
    console.log(age2020);


    //回调函数可以使用系统的内置函数
    var a = [25,36];
    var b = a.map(Math.sqrt);
    console.log(b);//[5,6]


    var re = [1,2,3].map(parseInt);
    console.log(re);//[1,NaN,NaN]

    console.log(parseInt(1, 0));//1
    console.log(parseInt(2, 1));//NaN
    console.log(parseInt(3, 2));//NaN
```


#### 19.数组过滤
- 使用filter方法可以返回数组中满足指定条件的元素。
- array.filter(function,thisArg)
- 返回值是一个包含回掉函数为其返回ture的所有值的新数组。如果回调函数为array的所有元素返回false，则新数组长度为0.
- 不会缺少的元素调用回调函数
```js
    // 筛选出所有的偶数
    var arr = [1,2,3,4,5,6,6,7,8,9];
    /*var evenArr = arr.filter(function (item,index,array) {
        return item % 2 == 0
    })
    console.log(evenArr);//[2,4,6,6,8]*/

    function f(item,index,array) {
        return item % 2 == 0;
    }
    var evenArr = arr.filter(f);
    console.log(evenArr);


    // 使用filter过滤掉不符合条件的值
    var obj = {max:80,min:14};
    var age = [12,11,34,56,90,92,65,65,34,31];
    var newAge = age.filter(function (item) {
        return item >= this.min && item <= this.max;
    },obj)
    console.log(newAge);

```


#### 20.reduce
- reduce方法可对数组的所有元素调用指定的回调函数。
- 该回调函数的返回值为累计结果，并且此返回值在下一次调用该回调函数的时候作为参  数提供
- reduce方法的参数函数可以是4个参数：上一次调用回调函数的返回值，如果提供了reduce的第二个参数，则第一次调用回调函数时，初始值是reduce方法的第二个参数；当前元数组元素的值；元素索引；数组对象
- reduce方法的最终返回值是通过最后一次调用回调函数获得的累计结果。
```js
    // 用-把数组的各个值分开‘
    var arr = ["abc","def","ggg","uuu"];
    var newStr = arr.reduce(function (a,b,c,d) {
        return a + "-" + b;
    },"oh")
    console.log(newStr);//oh-abc-def-ggg-uuu
    // 数组 arr = [1,2,3,4] 求数组的和
    var arr = [1,2,3,4];
    arr.reduce(function(pre,cur){return pre + cur}); // return 10

    // 计算数组最大值
    var max = arr.reduce(function (prev, cur) {
        return Math.max(prev,cur);
    });
```

#### 21.总结图片
<img src = https://upload-images.jianshu.io/upload_images/3532891-d94af0f1cd320a5a.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240>


#### 22.数组练习1：
```js
// 将数组的0去掉
    var arr = [1,3,4,0,6,4,0,4,5];
    var newArr = [];
    /*arr.forEach(function (item,index,array) {
        if (item == 0){
            // 当等于0的时候，我们不是要退出循环 而是退出这个函数
            return;
        }
        newArr.push(item);
    })
    console.log(newArr);*/
```
```js
    // 数组排序去重
    var arr = [1,3,2,2,4,2,1,6,4,2];
    // 先排序 后去重
    
    arr.sort(function (a,b) {
        return a-b;
    })
    console.log(arr);
    var newArr = [];
    for (var i = 0; i < arr.length; i++) {
        if (arr[i] == arr[i+1]){
            continue;
        }
        newArr.push(arr[i]);
    }
    console.log(newArr);
```

```js
    var arr = [1,3,56,43,78,32,67,34,0,87];
    var min = 100;
    var max = 0;
    for (var i = 0; i < arr.length; i++) {
        if (min > arr[i]){
            min = arr[i];
        }
        if (max < arr[i]){
            max = arr[i];
        }
    }
    console.log(min,max)
```

## 十一、定时器
### 01.setTimeout方法
- setTimeout方法能够在指定的时间段后执行特定代码(超时调用计时器)
- var o = setTimeout(code,delay);
- 参数code表示要延迟执行的字符串型代码,将在Window环境中执行,如果包含多个语句,应该使用分号进行分隔, delay表示延迟时间,以毫秒为单位
- setTimeout方法的第一个参数虽然是字符串，但是也可以是一个函数，一般建议把函数作为参数传递给setTimeout方法，等待延迟调用
- 如果setTimeout方法的第1个参数是一个函数,则 setTimeout方法可以接收任意多个参数,这些参数将作为该函数的参数使用
- 该方法返回值是一个 TimerID,这个ID编号指向延迟执行的代码控制句柄。如果把这个句柄传给 clearTimeout方法,则会取消代码的延迟执行
```js
    // code是一个字符串的书写格式
    window.setTimeout("alert(1)",1000)
    eval("alert(2)");



    // 如果code是一个函数的书写格式1
    window.setTimeout(function(){
        alert("延迟了2秒");
    },2000)



    // 如果code是一个函数的书写格式2
    function f() {
        alert("延迟了3秒");
    }
    window.setTimeout(f,3000)



    //传参的两种方法
    function f(a,b){
        alert(a+b)
    }
    var a = window.setTimeout("f(1,2)",1000)
    var b = window.setTimeout(f,1000,1,2);
    console.log(a, b);//计数器返回值是一个id


    function f1(a,b) {
        alert(a+b);
        return `alert(1)`;
    }
    setTimeout(f(1,2),3000);


    var oBtn = document.getElementById("btn");
    var timer1 = setTimeout(function () {
        alert("oh");
    },3000)
    oBtn.onclick = function () {
        clearTimeout(timer1);
    }

    // 当鼠标指针移过段落文本时,会延迟半秒钟弹出一个提示对话框
```
### 02.clearTimeout方法
- 利用cleartimeout方法在特定的条件下清除延迟处理代码。方法的参数是setTimeout方法的句柄
```html
<!-- 鼠标移入元素，元素下拉实现。当鼠标移出，延迟300毫秒消失。 -->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>超时计时器</title>
    <style>
        *{
            margin: 0;
            padding: 0;
            list-style: none;
        }
        #box{
            width: 300px;
            border: 1px solid #000;
            position: relative;
        }
        #box h2{
            height: 40px;
            background-color: red;
        }
        #con{
            width: 300px;
            height: 200px;
            position: absolute;
            left: 0;
            top:40px;
            background-color: #2ba5eb;
            display: none;
        }
    </style>
</head>
<body>
    <div id="box">
        <h2>我是标题</h2>
        <div id="con">
            我是内容
        </div>
    </div>
    <script>
        var oBox = document.getElementById("box");
        var oCon = document.getElementById("con");
        var timer = null;
        oBox.onmouseenter = function () {
            clearInterval(timer);
            oCon.style.display = "block";
        }
        oBox.onmouseleave = function () {
            // oCon.style.display = "none";
            timer = setTimeout(function () {
                oCon.style.display = "none";
            },300)
        }
    </script>
</body>
</html>
```

### 03.setInterval方法（间隙调用计时器）
- setInterval()方法能够周期性执行指定的代码，如果不加以处理，那么该方法将会被持续执行，直到浏览器窗口关闭或者跳转到其他页面为止。
- var o = setInterval(code,interval);
- 该方法的用法与setTimeout()方法基本相同,其中参数code表示要周期执行的代码字符串,参数interval表示周期执行的时间间隔,以毫秒为单位
- 该方法返回值是一个TimerID,这个ID编号指向对当前周期函数的执行引用,利用该值对计时器进行访问,如果把这个值传递给clearTimeout()方法,则会强制取消周期性执行的代码。
- 如果setInterval方法的第1个参数是一个函数,则 setInterval方法可以接收任意多个参数,这些参数将作为该函数的参数使用

### 04.clearInterval方法
- 利用clearInterval方法在特定的条件下清除延迟处理代码。方法的参数是setInterval方法的句柄
```html
<!-- // 书写一个倒计时10秒到达战场 -->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>间隙调用计时器</title>
</head>
<body>
    <h2 id="con">敌军还有<span id="sec">10</span>秒到达战场</h2>
<script>
    var oSec = document.getElementById("sec");
    var oCon = document.getElementById("con");
    var i = 10;
    var timer1 = setInterval(function () {
        i --;
        if (i <= 0){
            oCon.innerHTML = "全军出击";
            clearInterval(timer1);
        }
        oSec.innerHTML = i;
    },1000)
</script>
</body>
</html>
```

```html
<!-- 动画 -->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>间歇计时器案例</title>
    <style>
        #box{
            width: 100px;
            height: 100px;
            background-color: red;
            position: absolute;
            left: 0;
            top: 100px;
        }
    </style>
</head>
<body>
<button id="btn">点我看box走一下</button>
<div id="box">

</div>
<script>
    var oBox = document.getElementById("box");
    var oBtn = document.getElementById("btn");
    // 给一个变量保存当前元素的left值
    var oBoxLeft = 0;
    // 计时器一般在全局定义(因为你可能再其他的位置清计时器)
    var timer1 = null;//现在不使用 但是将来要使用 需要提前定义变量  可以给null
    oBtn.onclick = function () {
        /*一般我们保证一个运动只有一个计时器运行就可以了，但是我们每次重复点击，都会再额外的添加计时器进去
        所以我们在每次重复点击的时候，要把之前它身上的计时器给清掉，然后重新添加即可*/
        clearInterval(timer1);

        // 每隔多少毫秒 让box的定位值加一定的数值，可以达到动画效果
        // 一般控制元素的样式或者是位置，都是先对变量进行计算 然后再赋值过去
        timer1 = setInterval(function () {
            oBoxLeft ++;
            // 判断临界值使用变量判断即可
            if (oBoxLeft >= 1000){
                clearInterval(timer1);
            }
            oBox.style.left = oBoxLeft + "px";
        },1)
    }

</script>
</body>
</html>
```
#### 05.计时器函数的this指向
- this指向其所在函数的所有者(调用者)  如果没有所有者 则指向全局对象window
- 计时器函数是在window中运行的 计时器中的this基本上都是指向window的
```js
    setTimeout(function () {
        console.log(this);//window
    },1000)

    var obj = {
        fn1:function () {
            console.log(this);
        }
    }
    obj.fn1();//obj
    // 在这里 obj.fn1仅仅是保存了一个函数     然后我们点击了以后调用的函数  所以指向document
    document.onclick = obj.fn1;//document
    // 在这里 obj.fn1仅仅是保存了一个函数     然后浏览器到达一定时间调用函数  所以指向window
    setTimeout(obj.fn1,1000)//window
```

#### 06.计时器面试题
```js
// 面试题1

    /*计时器和事件一样 都是异步代码 。让同步代码（for）执行完成以后 才会去执行异步代码
    当去执行异步代码的时候 for已经执行完毕 i此时是5了。*/
    for (var i = 0; i < 5; i++) {
        setTimeout(function () {
            console.log(i);//5,5,5,5,5
        },0)
    }

    // 面试题2：对上边的代码进行修改，让弹出 0,1,2,3,4
    for (var i = 0; i < 5; i++) {
        (function fn(i) {
            //只要在这个函数中 出现i  那么就不会去使用for循环的i
            // 形参i 其实就是这个作用域的变量
            setTimeout(function () {
                console.log(i);
            },0)
        })(i);
    }
```

## 十一、脚本化CSS
### 01.设计大小
#### 01.offsetWidth和offsetHeight
- 使用offsetWidth和offsetHeight属性可以获取元素的尺寸(content+padding+border)
- offsetWidth表示元素在页面中所占用的总宽度，offsetHeight表示元素在页面中所占用的总高度。
- offsetWidth和offsetHeight是获取元素宽高最好的方法
- 当元素隐藏显示时，即设置样式属性display的值为none时，offsetWidth和offsetHeight返回的值是0
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>设计大小-offsetWidth和offsetHeight</title>
    <style>
        #box{
            width: 100px;
            height: 100px;
            background-color: red;
            padding: 20px;
            border: 1px solid #000;
            margin: 10px;
            /*display: none;*/
        }
    </style>
</head>
<body>
<div id="box"> </div>
<script>
    var oBox = document.getElementById("box");
    console.log(oBox.offsetWidth);
</script>
</body>
</html>
```

#### 02.clientWidth和clientHeight
- 获取元素可视部分的宽度，即css的content和padding属性的和，不包含任何能滚动的区域和边框
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>设计大小-clientWidth和clientHeight</title>
    <style>
        #box{
            width: 100px;
            height: 100px;
            background-color: red;
            padding: 20px;
            border: 1px solid #000;
            margin: 10px;
            /*display: none;*/
        }
    </style>
</head>
<body>
<div id="box"> </div>
<script>
    var oBox = document.getElementById("box");
    console.log(oBox.clientWidth);
</script>
</body>
</html>
```

#### 03.scrollWidth和scrollHeight
- 元素包含内容的完全宽度和padding
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>设计大小-scrollWidth和scrollHeight</title>
    <style>
        #box{
            width: 100px;
            height: 100px;
            background-color: red;
            padding: 20px;
            border: 1px solid #000;
            margin: 10px;
            overflow: auto;
            /*display: none;*/
        }
        #con{
            width: 10000px;
            height: 80px;
        }
    </style>
</head>
<body>
<div id="box">
    <div id="con"></div>
</div>
<script>
    var oBox = document.getElementById("box");
    console.log(oBox.scrollWidth);//10020
</script>
</body>
</html>
```

#### 04.获取窗口的大小
- 获取 `<html>`标签的clientWidth和clientHeight属性，就可以直到浏览器窗口的可是宽度和高度。
- 而获取html标签的脚本表示为document.documentElement
- 所以获取窗口宽度是 document.documentElement.clientWidth
- 在怪异模式下，body是最顶层的可视元素，所以在怪异模式下获取窗口的宽度是 document.body.clientWidth
- 兼容性代码就是：document.documentElement.clientWidth||document.body.clientWidth;
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>获取窗口的大小</title>
</head>
<body>
<script>
    
    var oHtml = document.getElementsByTagName("html")[0];
    var oBody = document.getElementsByTagName("body")[0];
    console.log(document.documentElement === oHtml);//true
    console.log(document.body === oBody);//true


    // 打印浏览器窗口的宽高
    console.log(document.documentElement.clientHeight);
    console.log(document.documentElement.clientWidth);


    //获取窗口高度的兼容性写法
    console.log(document.documentElement.clientWidth || document.body.clientWidth);
</script>
</body>
</html>
```
### 02.设计位置
#### 01.使用offsetLeft和offsetTop
- offsetLeft和offsetTop属性返回当前元素的偏移位置。DOM标准模式以最近的定位元素（包含块）为参考进行偏移的位置
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>设计位置-offsetLeft和offsetTop</title>
    <style>
        #outer{
            width: 500px;
            height: 500px;
            margin: 50px;
            overflow: hidden;
            background-color: red;
            padding: 10px;
            border: 1px solid #000;
            position: relative;
        }
        #inner{
            width: 300px;
            height: 300px;
            background-color: yellow;
            margin: 20px;
            padding: 10px;
            border: 1px solid #ccc;
            /*position: relative;*/

        }
        #con{
            width: 100px;
            height: 100px;
            margin: 10px;
            /*position: absolute;*/
            /*left: 40px;*/
            /*top: 40px;*/
            background-color: #0ee69c;
        }
    </style>
</head>
<body>
<div id="outer">
    <div id="inner">
        <div id="con"></div>
    </div>
</div>
<script>
    var oCon = document.getElementById("con");
    console.log(oCon.offsetLeft);
</script>
</body>
</html>
```

#### 02.offsetParent
- offsetParent属性表示最近的上级定位元素（包含块）
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>offsetParent</title>
    <style>
        #outer{
            width: 500px;
            height: 500px;
            margin: 50px;
            overflow: hidden;
            background-color: red;
            padding: 10px;
            border: 1px solid #000;
            position: relative;
        }
        #inner{
            width: 300px;
            height: 300px;
            background-color: yellow;
            margin: 20px;
            padding: 10px;
            border: 1px solid #ccc;
            position: relative;

        }
        #con{
            width: 100px;
            height: 100px;
            margin: 10px;
            /*position: absolute;*/
            /*left: 40px;*/
            /*top: 40px;*/
            background-color: #0ee69c;
        }
    </style>
</head>
<body>
<div id="outer">
    <div id="inner">
        <div id="con"></div>
    </div>
</div>
<script>
    var oCon = document.getElementById("con");
    console.log(oCon.offsetParent);
</script>
</body>
</html>
```

#### 03.scrollLeft和scrollTop
- 使用scrollLeft和scrollTop可以读写 移出可视区域外面的宽度和高度
- scrollLeft：读写元素左侧已经滚过的距离
- scrollTop：读写元素顶部已滚动的距离
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>scrollLeft和scrollTop</title>
    <style>
        #outer{
            width: 200px;
            height: 200px;
            border: 1px solid #000;
            overflow: auto;
        }
        #con{
            width: 2000px;
            height: 2000px;
            background-color: pink;
        }
    </style>
</head>
<body>
<button id="btn">点一哈</button>
<div id="outer">
    <div id="con"></div>
</div>
<script>
    var oOuter = document.getElementById("outer");
    var oBtn = document.getElementById("btn");
    oBtn.onclick = function () {
        // oOuter.scrollLeft = 200;
        console.log(oOuter.scrollLeft);
    }

</script>
</body>
</html>
```

#### 04.clientLeft和clientTop
- 边框的大小
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>设计位置-clientLeft和clientTop</title>
    <style>
        #outer{
            width: 500px;
            height: 500px;
            margin: 50px;
            overflow: hidden;
            background-color: red;
            padding: 10px;
            border: 1px solid #000;
            position: relative;
        }
        #inner{
            width: 300px;
            height: 300px;
            background-color: yellow;
            margin: 20px;
            padding: 10px;
            border: 1px solid #ccc;
            /*position: relative;*/

        }
        #con{
            width: 100px;
            height: 100px;
            margin: 10px;
            /*position: absolute;*/
            /*left: 40px;*/
            /*top: 40px;*/
            background-color: #0ee69c;
        }
    </style>
</head>
<body>
<div id="outer">
    <div id="inner">
        <div id="con"></div>
    </div>
</div>
<script>
    var oCon = document.getElementById("con");
    console.log(oCon.clientLeft);
    console.log(oCon.parentNode.clientLeft);
    console.log(oCon.parentNode.parentNode.clientLeft);
</script>
</body>
</html>
```

#### 04.获取窗口滚动条位置
```js
function getPS (){
    var h = document.documentElement;
    var x = self.pageXOffset||
            (h && h.scrollLeft)||
            document.body.scrollLeft;
    var y = self.pageYOffset||
            (h && h.scrollTop)||
            document.body.scrollTop;
    return {
        x:x,
        y:y
    }

}
```

#### 05.设置窗口滚动条位置
- 使用window对象的scrollTo(x,y)方法可以定位滚动条的位置
- 其中参数x可以定位页面内容在x轴方向上的偏移量。
```js
    function setWinScroll(n,m) {
        if (typeof m != "undefined" && typeof m =="number") {
            document.documentElement.scrollTop = m;
            document.body.scrollTop =m
        }
        if (typeof n != "undefined" && typeof n =="number") {
            document.documentElement.scrollLeft = n;
            document.body.scrollLeft = n;
        }
    }

    //或者：
    window.scrollTo(0,300);
```

#### 06.获取整个文档全文的宽高
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>-设计大小-获取整体文档的大小</title>
    <style>
        #outer{
            width: 200px;
            height: 2000px;
            border: 1px solid #000;
            overflow: auto;
        }
        #btn{
            position: fixed;
            left: 0;
            top: 50%;
        }
    </style>
</head>
<body>
<button id="btn">点一哈</button>
<div id="outer">

</div>
<script>
    var oOuter = document.getElementById("outer");
    var oBtn = document.getElementById("btn");
    oBtn.onclick = function () {
        console.log(document.documentElement.offsetHeight || document.body.offsetHeight);
    }

    function getDocSize() {
        return {
            height:document.documentElement.offsetHeight || document.body.offsetHeight,
            width:document.documentElement.offsetWidth || document.body.offsetWidth
        }
    }

</script>
</body>
</html>
```
#### 07.获取元素距离屏幕边缘的位置大小
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>offsetParent</title>
    <script src="./my.js"></script>
    <style>
        *{
            margin: 0;
            padding: 0;
        }
        #outer{
            width: 500px;
            height: 500px;
            margin: 50px;
            overflow: hidden;
            background-color: red;
            padding: 10px;
            border: 1px solid #000;
            position: relative;
        }
        #inner{
            width: 300px;
            height: 300px;
            background-color: yellow;
            margin: 20px;
            padding: 10px;
            border: 1px solid #ccc;
            position: relative;

        }
        #con{
            width: 100px;
            height: 100px;
            margin: 10px;
            /*position: absolute;*/
            /*left: 40px;*/
            /*top: 40px;*/
            background-color: #0ee69c;
        }
    </style>
</head>
<body>
<div id="outer">
    <div id="inner">
        <div id="con"></div>
    </div>
</div>
<script>
    /*
    * 获取元素具体屏幕边缘的位置大小
    * */
    var oCon = my.getID("con");
    console.log(oCon);

    /*// 第一步：
    var num = oCon.offsetLeft;

    // 第二步
    oCon = oCon.offsetParent;

    // 第三步：
    num += oCon.offsetLeft;

    // 第四步：
    oCon = oCon.offsetParent;

    //第五步：
    num += oCon.offsetLeft;*/


    function getEleToWin(ele) {
        var l = 0,t = 0;
        var oNewCon = ele;
        while(oNewCon){
            // 因为offsetLeft获取的是元素距离定位父级边框内侧的长度，所以，如果不是oCon，那么就要获取边框
            if (oNewCon == ele){
                l += oNewCon.offsetLeft;
                t += oNewCon.offsetTop;
                oNewCon = oNewCon.offsetParent;
            }else{
                l += oNewCon.offsetLeft + oNewCon.clientLeft;
                t += oNewCon.offsetTop + oNewCon.clientTop;
                oNewCon = oNewCon.offsetParent;
            }
        }
        return {left:l,top:t};
    }

    console.log(getEleToWin(oCon));
</script>

</body>
</html>
```

#### 08.封装my.js
```js
+function (w) {
    /*如果没有加号，解析器会认为function是一个函数声明的开始。在后边直接添加（）调用时错误的语法
    如果加上一个+号，就变成了一个函数表达式，后边添加（），就变成了立即执行函数*/
    // 当然波浪号和加号一个作用
    w.my = {};

    /*
        getWinScroll获取系统滚动条滚过去的距离 函数
        返回一个对象  对象的left属性保存横向滚动条滚过去的距离
        返回一个对象  对象的top属性保存竖向滚动条滚过去的距离
     */
    w.my.getWinScroll = function () {
        return {
            left:document.documentElement.scrollLeft||document.body.scrollLeft||window.pageXOffset,
            top:document.documentElement.scrollTop||document.body.scrollTop||window.pageYOffset
        }
    }

    /*
        setWinXScroll是设置横向系统滚动条滚过去的距离
        setWinYScroll是设置竖向系统滚动条滚过去的距离
        参数num 就是要设置的值
     */
    w.my.setWinXScroll = function(num){
        window.pageXOffset = num;
        document.documentElement.scrollLeft = num;
        document.body.scrollLeft = num;
    };
    w.my.setWinYScroll = function (num) {
        window.pageYOffset = num;
        document.documentElement.scrollTop = num;
        document.body.scrollTop = num;
    }


    /*
        getScreen()是获取浏览器可视化区域的宽度和高度
        可以直接调用返回对象的 width 和height 来获取
    */
    w.my.getScreen = function () {
        return {
            width:window.innerWidth||document.documentElement.clientWidth||document.body.clientWidth,
            height:window.innerHeight||document.documentElement.clientHeight||document.body.clientHeight
        }
    }

    /*
        getPreSibling(obj)获取 元素的上一个兄弟元素节点

     */
    w.my.getPreSibling = function(obj){
        return obj.previousElementSibling||obj.previousSibling;
    }

    /*
        getPreSibling(obj)获取 元素的上一个兄弟元素节点

     */
    w.my.getNextSibling = function(obj){
        return obj.nextElementSibling||obj.nextSibling;
    }

    /*
        getFirChild(obj)获取 元素第一个子元素节点

     */
    w.my.getFirChild = function(obj){
        return obj.firstElementChild||obj.firstChild;
    }

    /*
        getLastChild(obj)获取 元素的最后一个子元素节点

     */
    w.my.getLastChild = function(obj){
        return obj.lastElementChild||obj.lastChild;
    }
}(window)
```
## 十二、计时器效果练习1
### 01.无缝滚动
#### 01.无缝滚动布局
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>无缝滚动</title>
    <style>
        .outer{
            width: 965px;
            border: 1px solid #000;
            margin: 100px auto;
            overflow: scroll;
        }
        #inner{
            width: 2000px;
            overflow: hidden;
            position: relative;
            left: 0px;
        }
        #inner img{
            float: left;
            width: 193px;
            height: 136px;
        }
    </style>
</head>
<body>
    <div class="outer">
        <div id="inner">
            <img src="../images/01.jpg" alt="">
            <img src="../images/02.jpg" alt="">
            <img src="../images/03.jpg" alt="">
            <img src="../images/04.jpg" alt="">
            <img src="../images/05.jpg" alt="">
            <img src="../images/01.jpg" alt="">
            <img src="../images/02.jpg" alt="">
            <img src="../images/03.jpg" alt="">
            <img src="../images/04.jpg" alt="">
            <img src="../images/05.jpg" alt="">
        </div>
    </div>
    <script>
    </script>
</body>
</html>
```
#### 02.无缝滚动基础版
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>无缝滚动</title>
    <style>
        .outer{
            width: 965px;
            border: 1px solid #000;
            margin: 100px auto;
            overflow: scroll;
        }
        #inner{
            width: 2000px;
            overflow: hidden;
            position: relative;
            left: 0px;
        }
        #inner img{
            float: left;
            width: 193px;
            height: 136px;
        }
    </style>
</head>
<body>
    <div class="outer">
        <div id="inner">
            <img src="../images/01.jpg" alt="">
            <img src="../images/02.jpg" alt="">
            <img src="../images/03.jpg" alt="">
            <img src="../images/04.jpg" alt="">
            <img src="../images/05.jpg" alt="">
            <img src="../images/01.jpg" alt="">
            <img src="../images/02.jpg" alt="">
            <img src="../images/03.jpg" alt="">
            <img src="../images/04.jpg" alt="">
            <img src="../images/05.jpg" alt="">
        </div>
    </div>
    <script>
        var oInner = document.getElementById("inner");
        var timer = null;
        var oInnerLeft = 0;//定义left的初始值
        //刚进入页面 自动向左走
        timer = setInterval(function () {
            oInnerLeft +=1;
            if (oInnerLeft >= 193*5){
                oInnerLeft = 0;
            }
            oInner.style.left = - oInnerLeft + "px";
        },3)

    </script>
</body>
</html>
```
#### 02.无缝滚动按钮版
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>无缝滚动</title>
    <style>
        .outer{
            width: 965px;
            border: 1px solid #000;
            margin: 100px auto;
            overflow: hidden;
        }
        #inner{
            width: 2000px;
            overflow: hidden;
            position: relative;
            left: 0px;
        }
        #inner img{
            float: left;
            width: 193px;
            height: 136px;
        }
    </style>
</head>
<body>
    <button id="left">向左走</button>
    <button id="right">向右走</button>
    <button id="stop">停止</button>
    <div class="outer">
        <div id="inner">
            <img src="../images/01.jpg" alt="">
            <img src="../images/02.jpg" alt="">
            <img src="../images/03.jpg" alt="">
            <img src="../images/04.jpg" alt="">
            <img src="../images/05.jpg" alt="">
            <img src="../images/01.jpg" alt="">
            <img src="../images/02.jpg" alt="">
            <img src="../images/03.jpg" alt="">
            <img src="../images/04.jpg" alt="">
            <img src="../images/05.jpg" alt="">
        </div>
    </div>
    <script>
        var oInner = document.getElementById("inner");
        var oLeft = document.getElementById("left")
        var oRight = document.getElementById("right")
        var oStop = document.getElementById("stop")
        var timer = null;
        var oInnerLeft = 0;//定义left的初始值
        //刚进入页面 自动向左走
        timer = setInterval(function () {
            oInnerLeft +=1;
            if (oInnerLeft >= 193*5){
                oInnerLeft = 0;
            }
            oInner.style.left = - oInnerLeft + "px";
        },3)

        //点击向左走
        oLeft.onclick = function () {
            /*每次点击都会叠加计时器，我们在每次点击添加新的计时器之前，先把原来的计时器给清除掉
            因为整个运动使用的是同一个oInnerLeft，所以下次运动仍然能接着之前的继续执行*/
            clearInterval(timer)
            timer = setInterval(function () {
                oInnerLeft +=1;
                if (oInnerLeft >= 193*5){
                    oInnerLeft = 0;
                }
                oInner.style.left = - oInnerLeft + "px";
            },3)
        }

        // 点击向右走
        oRight.onclick = function(){
            clearInterval(timer);
            timer = setInterval(function () {
                oInnerLeft -= 1;
                if (oInnerLeft <= 0){
                    oInnerLeft = 193 * 5;
                }
                oInner.style.left = - oInnerLeft + "px";
            },3)
        }

        //点击停止按钮 让动画停止
        oStop.onclick = function () {
            clearInterval(timer);
        }
    </script>
</body>
</html>
```
#### 03.无缝滚动鼠标控制版本
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>无缝滚动</title>
    <style>
        .outer{
            width: 965px;
            border: 1px solid #000;
            margin: 100px auto;
            overflow: hidden;
        }
        #inner{
            width: 2000px;
            overflow: hidden;
            position: relative;
            left: 0px;
        }
        #inner img{
            float: left;
            width: 193px;
            height: 136px;
        }
    </style>
</head>
<body>
    <button id="left">向左走</button>
    <button id="right">向右走</button>
    <button id="stop">停止</button>
    <div id="outer" class="outer">
        <div id="inner">
            <img src="../images/01.jpg" alt="">
            <img src="../images/02.jpg" alt="">
            <img src="../images/03.jpg" alt="">
            <img src="../images/04.jpg" alt="">
            <img src="../images/05.jpg" alt="">
            <img src="../images/01.jpg" alt="">
            <img src="../images/02.jpg" alt="">
            <img src="../images/03.jpg" alt="">
            <img src="../images/04.jpg" alt="">
            <img src="../images/05.jpg" alt="">
        </div>
    </div>
    <script>
        var oInner = document.getElementById("inner");
        var oOuter = document.getElementById("outer");
        var oLeft = document.getElementById("left")
        var oRight = document.getElementById("right")
        var oStop = document.getElementById("stop")
        var timer = null;
        var flag = true;//定义一个开关 保存动画的运动方向  默认向左走为true
        var oInnerLeft = 0;//定义left的初始值
        //刚进入页面 自动向左走
        timer = setInterval(function () {
            oInnerLeft +=1;
            if (oInnerLeft >= 193*5){
                oInnerLeft = 0;
            }
            oInner.style.left = - oInnerLeft + "px";
        },3)

        //点击向左走
        oLeft.onclick = function () {
            /*每次点击都会叠加计时器，我们在每次点击添加新的计时器之前，先把原来的计时器给清除掉
            因为整个运动使用的是同一个oInnerLeft，所以下次运动仍然能接着之前的继续执行*/
            clearInterval(timer)
            // 只要点击向左走，就让开关为true
            flag = true;
            timer = setInterval(function () {
                oInnerLeft +=1;
                if (oInnerLeft >= 193*5){
                    oInnerLeft = 0;
                }
                oInner.style.left = - oInnerLeft + "px";
            },3)
        }

        // 点击向右走
        oRight.onclick = function(){
            clearInterval(timer);
            // 只要向右走，就让开关flag为false
            flag = false;
            timer = setInterval(function () {
                oInnerLeft -= 1;
                if (oInnerLeft <= 0){
                    oInnerLeft = 193 * 5;
                }
                oInner.style.left = - oInnerLeft + "px";
            },3)
        }

        //点击停止按钮 让动画停止
        oStop.onclick = function () {
            clearInterval(timer);
        }


        // 鼠标移入动画 动画停止
        oOuter.onmouseenter = function () {
            clearInterval(timer);
        }

        // 鼠标移出，元素继续接着停止之前的方向移动
        oOuter.onmouseleave = function () {
            if (flag){
                timer = setInterval(function () {
                    oInnerLeft +=1;
                    if (oInnerLeft >= 193*5){
                        oInnerLeft = 0;
                    }
                    oInner.style.left = - oInnerLeft + "px";
                },3)
            } else {
                timer = setInterval(function () {
                    oInnerLeft -= 1;
                    if (oInnerLeft <= 0){
                        oInnerLeft = 193 * 5;
                    }
                    oInner.style.left = - oInnerLeft + "px";
                },3)
            }
        }
    </script>
</body>
</html>
```
#### 05.无缝滚动函数封装
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>无缝滚动</title>
    <style>
        .outer{
            width: 965px;
            border: 1px solid #000;
            margin: 100px auto;
            overflow: hidden;
        }
        #inner{
            width: 2000px;
            overflow: hidden;
            position: relative;
            left: 0px;
        }
        #inner img{
            float: left;
            width: 193px;
            height: 136px;
        }
    </style>
</head>
<body>
    <button id="left">向左走</button>
    <button id="right">向右走</button>
    <button id="stop">停止</button>
    <div id="outer" class="outer">
        <div id="inner">
            <img src="../images/01.jpg" alt="">
            <img src="../images/02.jpg" alt="">
            <img src="../images/03.jpg" alt="">
            <img src="../images/04.jpg" alt="">
            <img src="../images/05.jpg" alt="">
            <img src="../images/01.jpg" alt="">
            <img src="../images/02.jpg" alt="">
            <img src="../images/03.jpg" alt="">
            <img src="../images/04.jpg" alt="">
            <img src="../images/05.jpg" alt="">
        </div>
    </div>
    <script>
        var oInner = document.getElementById("inner");
        var oOuter = document.getElementById("outer");
        var oLeft = document.getElementById("left")
        var oRight = document.getElementById("right")
        var oStop = document.getElementById("stop")
        var timer = null;
        var flag = true;//定义一个开关 保存动画的运动方向  默认向左走为true
        var oInnerLeft = 0;//定义left的初始值

        function moveLeft(){
            timer = setInterval(function () {
                oInnerLeft +=1;
                if (oInnerLeft >= 193*5){
                    oInnerLeft = 0;
                }
                oInner.style.left = - oInnerLeft + "px";
            },3)
        }
        function moveRight(){
            timer = setInterval(function () {
                oInnerLeft -= 1;
                if (oInnerLeft <= 0){
                    oInnerLeft = 193 * 5;
                }
                oInner.style.left = - oInnerLeft + "px";
            },3)
        }
        //刚进入页面 自动向左走
        moveLeft();
        //点击向左走
        oLeft.onclick = function () {
            clearInterval(timer)
            flag = true;
            moveLeft();
        }

        // 点击向右走
        oRight.onclick = function(){
            clearInterval(timer);
            // 只要向右走，就让开关flag为false
            flag = false;
            moveRight();
        }

        //点击停止按钮 让动画停止
        oStop.onclick = function () {
            clearInterval(timer);
        }


        // 鼠标移入动画 动画停止
        oOuter.onmouseenter = function () {
            clearInterval(timer);
        }

        // 鼠标移出，元素继续接着停止之前的方向移动
        oOuter.onmouseleave = function () {
            if (flag){
                moveLeft();
            } else {
                moveRight();
            }
        }
    </script>
</body>
</html>
```
#### 06.无缝滚动间歇版
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>无缝滚动</title>
    <style>
        .outer{
            width: 1005px;
            border: 1px solid #000;
            margin: 100px auto;
            overflow: hidden;
        }
        #inner{
            width: 2100px;
            overflow: hidden;
            position: relative;
            left: 0px;
        }
        #inner img{
            float: left;
            width: 193px;
            height: 136px;
            margin-right: 10px;
        }
    </style>
</head>
<body>
    <button id="left">向左走</button>
    <button id="right">向右走</button>
    <button id="stop">停止</button>
    <div class="outer">
        <div id="inner">
            <img src="../images/01.jpg" alt="">
            <img src="../images/02.jpg" alt="">
            <img src="../images/03.jpg" alt="">
            <img src="../images/04.jpg" alt="">
            <img src="../images/05.jpg" alt="">
            <img src="../images/01.jpg" alt="">
            <img src="../images/02.jpg" alt="">
            <img src="../images/03.jpg" alt="">
            <img src="../images/04.jpg" alt="">
            <img src="../images/05.jpg" alt="">
        </div>
    </div>
    <script>
        var oInner = document.getElementById("inner");
        var oLeft = document.getElementById("left")
        var oRight = document.getElementById("right")
        var oStop = document.getElementById("stop")
        var timer = null,timer2 = null;
        var oInnerLeft = 0;//定义left的初始值
        //刚进入页面 自动向左走
        function moveLeft(){
            timer = setInterval(function () {
                oInnerLeft +=1;
                //每当走过去一张的距离的时候，就停一下（清计时器）
                if (oInnerLeft % (193+10)==0) {
                    clearInterval(timer);
                    timer2 = setTimeout(function () {
                        moveLeft();
                    },1000)
                }
                //当走到临界值 就跳到0
                if (oInnerLeft >= (193+10)*5){
                    oInnerLeft = 0;
                }
                oInner.style.left = -oInnerLeft + "px";
            },3)
        }

        //刚进入页面 自动向右走
        function moveRight(){
            timer = setInterval(function () {
                oInnerLeft -=1;
                //每当走过去一张的距离的时候，就停一下（清计时器）
                if (oInnerLeft % (193+10) == 0) {
                    clearInterval(timer);
                    timer2 = setTimeout(function () {
                        moveRight();
                    },1000)
                }
                //当走到临界值 就跳到0
                if (oInnerLeft <= 0){
                    oInnerLeft = (193+10)*5;
                }
                oInner.style.left = -oInnerLeft + "px";
            },3)
        }

        function clear() {
            clearInterval(timer);
            clearInterval(timer2);
        }


        //打开页面自动走
        moveLeft();
        //点击向左走
        oLeft.onclick = function () {
            clear();
            moveLeft();
        }

        // 点击向右走
        oRight.onclick = function(){
            clear();
            moveRight()
        }

        //点击停止按钮 让动画停止
        oStop.onclick = function () {
            clear();
        }
    </script>
</body>
</html>
```




































### 02.碰壁反弹
#### 01.方法1
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>碰壁反弹</title>
    <style>
        #outer{
            width: 900px;
            height: 400px;
            background-color: #ccc;
            position: relative;
            margin: 0 auto;
            border:1px solid #000;
        }
        #box{
            width: 50px;
            height: 50px;
            background-color: indianred;
            position: absolute;
            left: 30px;
            top: 60px;
        }
    </style>
</head>
<body>
<div id="outer">
    <div id="box">

    </div>
</div>
<script>
    var oOuter = document.getElementById("outer");
    var oBox = document.getElementById("box");
    var timer = null;
    // 定义一个变量 保存x轴的位置
    var leftPoint = 30,topPoint = 60;
    //定义一个开关，如果目前向右走  那么值为true
    var isRight = true,isBottom = true;
    timer = setInterval(function () {
        if (isRight) {
            leftPoint ++;
            // 父级的宽度 减去 box 的宽度 就是box向右走最大的距离  临界值
            if (leftPoint >= oOuter.clientWidth - oBox.offsetWidth) {
                isRight = !isRight;
            }
        }else{
            leftPoint --;
            if (leftPoint <= 0){
                isRight = !isRight;
            }
        }


        if (isBottom) {
            topPoint ++;
            // 父级的宽度 减去 box 的宽度 就是box向右走最大的距离  临界值
            if (topPoint >= oOuter.clientHeight - oBox.offsetHeight) {
                isBottom = !isBottom;
            }
        }else{
            topPoint --;
            if (topPoint <= 0){
                isBottom = !isBottom;
            }
        }
        oBox.style.left = leftPoint + "px";
        oBox.style.top = topPoint + "px";
    },1)
</script>
</body>
</html>
```

#### 02.方法2
```html
<body>
    <div class="wrap">
        <div class="box"></div>
    </div>

<script>
    // 获取元素
    var wrap = document.getElementsByTagName("div")[0];
    var box = document.getElementsByTagName("div")[1]; 

    //让元素动起来
    // 添加两个变量，用于更换运动方向
    var a = 1;
    var b = 1;
    // 获取元素的可运动空间，用父元素的宽高减去子元素的宽高
    var w = wrap.offsetWidth - box.offsetWidth;
    var h = wrap.offsetHeight - box.offsetHeight;

    // console.log(w,h);
    
    setInterval(function(){
        // 获取元素当前left
        var  l  = box.offsetLeft;
        if(l == w || l == 0){
            // 如果到达可运动空间最大值和最小值的时候，a 变成负值
            a *= -1;
        }
        // 把元素距离左边的值每10ms加1px
        // a变成负值可以改变运动方向
        box.style.left = l + a + "px";

        // 垂直方向同水平方向
        var t = box.offsetTop;
        if(t == h || t == 0){
            b *= -1;
        }
        box.style.top = t + b + "px";
    },10); 

</script>
</body>
```
### 03.回到顶部
#### 01.基础版本
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>回到顶部基础版</title>
    <style>
        .box{
            width: 140px;
            height: 80px;
            background-color: red;
            border-radius: 50%;
            text-align: center;
            line-height: 80px;
            display: none;

            position: fixed;
            right: 0;
            bottom: 0;
        }

        .con{
            height: 3000px;
        }
    </style>
</head>
<body>
    <div class="box">
        回到顶部
    </div>
    <div class="con">

    </div>
    <script>
        /*
        * 当滚动条的的距离没有大于200px的时候，box按钮不显示
        *
        * onscroll 是当滚动的时候触发事件
        * */
        var oBox = document.getElementsByClassName("box")[0];
        window.onscroll = function () {
            // console.log(1);
            if ((window.pageYOffset||document.documentElement.scrollTop||document.body.scrollTop) >= 200){
                oBox.style.display = "block";
            }else{
                oBox.style.display = "none";
            }
        }

        //点击box 直接让页面回到顶部   直接让滚轮变成0即可
        oBox.onclick = function () {
            window.scrollTo(0,0);
        }

    </script>
</body>
</html>
```
#### 02.方法1
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>回到顶部</title>
    <style>
        body{
            height: 4000px;
            background-color: #cccc;
            position: relative;
        }
        #box{
            width: 100px;
            height: 40px;
            border-radius: 50%;
            background-color: red;
            position: fixed;
            right: 10px;
            bottom: 10px;
            text-align: center;
            line-height: 40px;
            color: #fff;
            /*让鼠标变成小手*/
            cursor: pointer;
        }
    </style>
</head>
<body>
<div id="box">
    回到顶部
</div>
<script src="./my.js"></script>
<script>
    var oBox = document.getElementById("box");
    var timer = null;
    oBox.onclick = function () {
        var nowScroll = my.getWinScroll().top;
        timer = setInterval(function () {
            nowScroll -= 20;
            if (nowScroll <= 0){
                nowScroll = 0;
                clearInterval(timer);
            }
            my.setWinYScroll(nowScroll);
        },1)
    }
</script>
</body>
</html>
```
#### 03.方法2
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>回到顶部进阶版</title>
    <style>
        body{
            height: 4000px;
            background-color: #cccc;
            position: relative;
        }
        #box{
            width: 100px;
            height: 40px;
            border-radius: 50%;
            background-color: red;
            position: fixed;
            right: 10px;
            bottom: 10px;
            text-align: center;
            line-height: 40px;
            color: #fff;
            /*让鼠标变成小手*/
            cursor: pointer;
        }
    </style>
</head>
<body>
<div id="box">
    回到顶部
</div>
<script src="./my.js"></script>
<script>
    console.log(my)
    var oBox = document.getElementById("box");
    var timer = null;
    oBox.onclick = function () {
        clearInterval(timer);
        //获取起始位置
        var start = my.getWinScroll().top;
        //获取结束位置
        var end = 0;
        //设置起始步数
        var startStep = 0;
        //设置总步数
        var endStep = 40;
        //计算每一步所走的距离
        var everyStep = (end - start) / (endStep - startStep);
        //进入计时器  让计时器每次运行都走 everyStep的距离  总共走endStep次 就可以执行完
        // console.log(window.pageYOffset)
        timer = setInterval(function () {
            // 每次进入计时器 让startStep++  用来保存执行次数
            startStep ++;
            // 临界值 当startStep等于endStep  那么说明运动完成
            if (startStep >= endStep){
                startStep = 0;
                clearInterval(timer);
            }
            start += everyStep;
            my.setWinYScroll(start);
        },16)


    }
</script>
</body>
</html>
```

## 十三、BOM
### 01.什么是BOM
- 浏览器对象模型（Browser Object Model）。主要用在客户端浏览器的管理。
- 一直没有被标准化，不过各个主流浏览器都支持BOM
- 它使 javascript 有能力与浏览器进行“对话”。

### 02.window对象
- window是客户端浏览器对象模型的基类。
- window对象是客户端JS的全局对象。
- 一个window对象实际上就是一个独立的窗口,对于框架页面来说,浏览器窗口中每个框架都包含一个 window对象
- 在客户端浏览器中, window对象是访问BOM的接口,如引用 document对象的document属性,引用自身的 window和self属性等
#### 01.全局作用域
window也为客户端 JavaScript提供全局作用域
```js
    // 定义全局作用域
    /*window.a = 1;
    window.f1 = function () {
        alert(2);
    }
    console.log(a);
    f1();*/

    // console.log(b,c,d);//全部报错 找不到变量
    /*function f1(){
        var a = b = c = d = 2;
        console.log(a,b,c,d);//2 2 2 2
    }
    f1();
    console.log(b,c,d);// 2 2 2

    var h ;
    console.log(h = 10);//赋值操作返回赋值的那个值*/
```

#### 02.访问客户端对象
- 使用 window对象可以访问客户端其他对象,这种关系构成浏览器对象模型。
>navigator:包含客户端有关浏览器的信息
screen：包含客户端屏幕的信息
history：包含浏览器窗口访问过的URL信息
location：包含当前网页文档的URL信息
document：包含整个HTML文档，可以用来访问文档内容及其所有页面元素

#### 03.使用系统对话框
window对象定义了3个人机交互的方法,主要方便对 JavaScript代码进行测试：
- alert:确定提示框。由浏览器向用户弹出提示性信息。该方法包含一个可选的提示信息参数如果没有指定参数,则弹出一个空的对话框
- confirm:选择提示框。由浏览器向用户弹出提示性信息,弹出的对话框中包含两个按钮,分别表示“确定”和“取消”。如果单击“确定”按钮,则该方法将返回true;单击“取消”按钮,则返回false. confirm方法也包含一个可选的提示信息参数,如果没有指定参数,则弹出一个空的对话框
- prompt:输入提示框。可以接收用户输入的信息,并返回输入的信息。 prompt方法也包含个可选的提示信息参数,如果没有指定参数,则弹出一个没有提示信息的输入文本对话框

```js
//请输入用户名，请确认，欢迎您
```

#### 04.打开和关闭窗口
- 使用window对象的open()方法可以打开一个新窗口
- window.open(url,name,features)
- url 可选字符串，新页面的地址，如果省略则是空白页面
- name 可选字符串 声明新窗口的名称。如果指定的是一个已经有的窗口，则open方法不会创建一个新的窗口。
- features 可选字符串 声明了新窗口要现实的浏览器特征 top width resizable：yes/no/1/0 status location left height fullscreen

- 使用window的close()方法可以关闭一个窗口
- 使用window.closed方法 可以检测窗口是否关闭
```js
    // window.open是用来打开一个窗口
    /*open方法的参数  3个：
        url：需要载入的地址
        新窗口的名称：_self  _blank
        新窗口的属性：窗口的大小  位置*/

    var oBtn1 = document.getElementById("btn1");
    var oBtn2 = document.getElementById("btn2");
    var newWin = null;
    oBtn1.onclick = function () {
        // 当书写新窗口打开 并且书写窗口大小位置的时候，会开一个新的浏览器窗口
        // window.open("http://www.baidu.com","_blank","width=300,height=300,left=200,top=100");


        // 当不写第三个参数的时候，_blank是打开一个新的标签页
        // window.open 返回一个值代表的是这个窗口，可以供我们对窗口操作
        newWin = window.open("http://www.baidu.com","_blank");
    }


    // close();是关闭一个窗口 如果关闭谁 就让谁调用close方法
    // 如果关闭自身 那就使用  window.close()

    oBtn2.onclick = function () {
        // 关闭新窗口
        // newWin.close();

        // 关闭自身
        window.close();
    }
```
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
    <button id="btn">点我付款</button>
    <script>
        var oBtn = document.getElementById("btn");
        oBtn.onclick = function () {
            alert("付款成功");
            window.open("./demo.html","newWin","top=0px")
        }
    </script>
</body>
</html>
```

### 03.navigator对象
- navigator对象存储了与浏览器相关的基本信息,如名称、版本和系统等,通过 window.navigator可以引用该对象,并利用它的属性来读取客户端基本信息
#### 01.浏览器检测方法
- 检测浏览器类型的方法有多种,常用的方法包括两种:特征检测法和字符串检测法,这两种方法都存在各自的优点与缺点,用户可以根据需要进行选择.
##### 01.特征检测法
- 特征检测法就是根据浏览器是否支持特定功能来决定相应操作的方式。这是一种非精确判断法,ww 。但却是最安全的检测方法,
- 因为准确检测浏览器的类型和型号是一件很困难的事情,而且很容易存在误差,如果不关心浏览器的身份,仅仅在意浏览器的执行能力,那么使用特征检测法就完全可以满足需要
- 当使用一个对象、方法或属性时,先判断它是否存在,如果存在,则说明浏览器支持该对象、方法属性,那么就可以放心使用
```js
    if (document.documentElement){
        var w = document.documentElement.clientWidth
    } else{
        var w = document.body.clientWidth
    }
```
##### 02.字符串检测法
- 客户端浏览器每次发送HTTP请求时,都会附带有一个user-agent(用户代理)字符串,对于Web开发人员来说,可以使用用户代理字符串检测浏览器类型
userAgent字符串包含了web浏览器的大量信息，如浏览器的名称和版本。
```js
var ua = navigator.userAgent.toLowerCase();
var info = {
    ie:/msie/.test(ua) && !/opera/.test(ua),
    op:/opera/.test(ua),
    sa:/version.*safari/.test(ua),
    ch:/chrome/.test(ua),
    ff:/gecko/.test(ua) && !/webkit/.test(ua)
}
info.ie && console.log("ie");
info.op && console.log("op");
info.sa&& console.log("sa");
info.ch && console.log("ch");
info.ff && console.log("ff");
```

#### 02.浏览器的类型和版本号
- 检测浏览器的类型和版本就比较容易了，用户只需要根据不用浏览器类型匹配特殊信息即可。
```js
// 获取IE版本号：
function getIEVer(){
    var ua = navigator.userAgent;
    var b = ua.indexOf("MSIE");
    if(b<0){
        return 0;
    }
    return parseFloat(ua.substring(b+5,ua.indexOf(";",b)))
}

```

#### 03.检测操作系统
- navigator.userAgent返回值一般都会包含操作系统的基本信息,不过这些信息比较散乱,没有统一的规则。
- 用户可以检测一些更为通用的信息,如检测是否为 Windows系统,或者为 Macintosh系统,而不去分辨操作系统的版本号
- 例如,如果仅检测通用信息,那么所有 Windows版本的操作系统都会包含"Win”字符串,所有Macintosh版本的操作系统都包含有"Mac”字符串,所有Umix版本的操作系统都包含有"X11”,而 Linux操作系统会同时包含"X11”和" Linux
```js

//如果仅检测通用信息，那么所有Windows版本的操作系统都会包含"Win"字符串，而所有的Macintosh版本操作系统都包含有"Mac"字符串，所有的UNIX版本操作系统都包含有"X11"，而在Linux操作系统下则同时包含"X11"和"Linux"。所以，用户可以通过快速检测用户端信息中是否包含上述字符串来进行准确判断：
var isWin = (navigator.userAgent.indexOf("Win") != - 1);
	// 如果是Windows系统，则返回true
var isMac = (navigator.userAgent.indexOf("Mac") != - 1); 
	// 如果是Macintosh系统，则返回true 
var isUnix = (navigator.userAgent.indexOf("X11") != - 1); 
	// 如果是UNIX系统，则返回true
var isLinux = (navigator.userAgent.indexOf("Linux") != - 1); 
	// 如果是Linux系统， xc则返回true
```

- platform 属性是一个只读的字符串，声明了运行浏览器的操作系统和（或）硬件平台。

### 04.location对象
- location对象存储了与当前文档位置(URL)相关的信息,简单地说就是网页地址字符串,使用 window对象的loaction属性可以访问
- location对象定义了8个属性,其中7个属性可以获取当前URL的各部分信息,另一个属性(href)包含了完整的URL信息
-  > href : 声明或获取当前文档完整的URL
    protocol:协议部分包括后缀的冒号。例如http:
    host:主机和端口名称 www.baidu.com:8080
    hostname:主机名称
    port：端口号
    pathname 路径部分
    search：url的查询部分，包括前导问号
    hash：锚部分包括前导 #

- location还定义两三方法：reload()和replace() assign()
    assign:和href相当
    reload:重新加载文档
    replace：可以装载一个新文档而无须为它创建一个新的历史记录。替换当前文档的历史记录
```js
// location对象属性(哈希值在地址栏中不会影响页面的跳转 浏览器在请求服务器时是不管他的)
    console.log(location.hash);

    // host:主机名：端口号
    console.log(location.host);//localhost:63342

    //hostname:主机名
    console.log(location.hostname);//localhost

    // prot：端口号
    console.log(location.port);//63342

    // pathname:路径名  在服务器中 当前页面的路径名称
    console.log(location.pathname);

    // href：url地址 完整路径
    console.log(location.href);

    // search 查询字符串  路径问号后跟的数据
    console.log(location.search);



    // location的方法
    var oBtn1 = document.getElementById("btn1");
    var oBtn2 = document.getElementById("btn2");
    var oBtn3 = document.getElementById("btn3");
    oBtn1.onclick = function () {
        location.assign("http://www.baidu.com");
    }
    oBtn2.onclick = function () {
        location.replace("http://www.baidu.com");
    }
    oBtn3.onclick = function () {
        // location.reload(true);//硬刷新
        location.reload(false);
    }
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>倒计时跳转</title>
</head>
<body>
<button id="btn">点击我注册成功</button>
<h2><span id="time">5</span>秒后进行跳转</h2>
<script>
    var oBtn = document.getElementById("btn");
    var oTime = document.getElementById("time");
    var timer = null;
    oBtn.onclick = function () {
        var reduceTime = 5;
        timer = setInterval(function () {
            reduceTime --;
            oTime.innerHTML = reduceTime;
            if(reduceTime <=0 ){
                clearInterval(timer)
                // location.href 也可以设置页面跳转
                location.href = "http://www.baidu.com";
                // location.assign("http://www.baidu.com");
                // location.replace("http://www.baidu.com");
                // window.open("http://www.baidu.com");
            }

        },1000)
    }
</script>
</body>
</html>
```

### 05.history对象
- history对象存储了客户端浏览器的浏览历史，通过window对象的history属性可以访问该对象
- 在历史记录中后退：window.history.back(),相当于返回
- 在历史记录中前进：window.history.forward(),相当于前进
- 移动到指定的历史记录点，使用go方法从当前会话的历史记录中加载页面。上一页就是-1，上上一页就是-2
- length属性可以了解历史记录栈中一共有多少页 window.history.length
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>01</title>
</head>
<body>
<h1>01</h1>
<a href="02.html">02</a>
<a href="03.html">03</a>
<button id="forward">前进</button>
<button id="back">后退</button>
<button id="go">揍你</button>
<script>
    var oForward = document.getElementById("forward");
    var oBack= document.getElementById("back");
    var oGo = document.getElementById("go");
    oForward.onclick = function () {
        history.forward();
    }

    oBack.onclick = function () {
        history.back();
    }
    oGo.onclick = function () {
        history.go(-2)
    }
</script>
</body>
</html>
```

## 十四、DOM
### 01.什么是 DOM
- DOM( Document Object Model,文档对象模型)是w3C制订的一套技术规范,用来描述 Javascript脚本如何与HTML或XML文档进行交互的Web标准
- 加载 HTML 页面时, Web浏览器生成一个树型结构,用来表示页面内部结构。DOM 将这种树型结构理解为由节点组成的DOM树
- DOM规定了一系列标准接口,允许开发人员通过标准方式访问文档结构、操作网页内容、控制样式和行为等
<img src=https://upload-images.jianshu.io/upload_images/3532891-7d056b97bb54ed30.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240>

### 02.DOM基础
- 在W3C推出DOM标准之前,市场上已经流行了不同版本的DOM规范,主要包括IE和 Netscape两个浏览器厂商各自制订的私有规范,这些规范定义了一套文档结构操作的基本方法。虽然这些规范存在差异,但是思路和用法基本相同,如文档结构对象、事件处理方式、脚本化样式等。习惯上,我们把这些规范称为DOM0级,虽然这些规范没有统一并实现标准化,但是得到所有浏览器的支持并被广泛应用
- 1998年W3C对DOM进行标准化,并先后推出了3个不同的版本,每个版本都是在上一个版本的基础上进行完善和扩展。但是在某些情况下,不同版本之间可能会存在不兼容的规定
>1)DoM1级:1998年10月,W3C推出DOM1.0版本规范,作为推荐标准进行正式发布,主要包括两个子规范
    DOM Core(核心部分):把XML文档设计为树形节点结构,并为这种结构的运行机制制订了套规范化标准,同时定义了创建、编辑、操纵这些文档结构的基本属性和方法
    DOM HTML:针对HTML文档、标签集合,以及与个别HTML标签相关的元素定义了对象属性和方法
>2).DOM2级:2000年11月,W3C正式发布了更新后的DOM核心部分,并在这次发布中添加了一些新规范,于是人们就把这次发布的DOM称为2级规范,2003年1月,W3C又正式发布了对 DOM HTML子规范的修订,添加了针对HTML4.01和 XHTML1.0版本文档中很多对象、属性和方法.W3C把新修订的DOM规范统一称为DOM2.0推荐版本,该版
本主要包括6个推荐子规范
    DOM2core:继承于 DOM Core子规范,规定了DOM文档结构模型,添加了更多的特性,如针对命名空间的方法等
    DOM2HTML:继承于 DOM HTML,规定了针对HTML的DOM文档结构模型,并添加了一些属性
    DOM2 Events:规定了与鼠标相关的事件(包括目标、捕获、冒泡和取消)的控制机制,但不含与键盘相关事件的处理部分
    DOM2Style(或DOM2Css):提供了访问和操纵所有与Css相关的样式及规则的能力
    DOM2 Traversal和DOM2 Range:DoM2 Traversal规范允许开发人员通过迭代方式访问DOM
    DOM2vews:提供了访问和更新文档表现(视图)的能力。
>3).DoM3级:2004年4月,W3C发布了DOM3版本,DOMB3版本主要包括以下3个推荐子规范
    DOM3Core:继承于DOM2Core,并添加了更多的新方法和属性,同时修改了已有的一些方法
    DOM3 Load and Save:提供将XML文档的内容加载到DOM文档中,以及将DOM文档序列化为XML文档的能力
    DOM3 Validation:提供了确保动态生成的文档的有效性的能力,即如何符合文档类型声明

### 03.节点
- 在网页中所有对象和内容都被称为节点,如文档、元素、文本、属性、注释等。节点(Node)是DOM最基本的单元,并派生出不同类型的节点,它们共同构成了文档的树形结构模型。
#### 01.节点类型(常用)
- document 文档节点 根节点 9
- documentFragment 文档片段 11
- Element 元素节点  1
- attr 属性节点  2
- text 文本节点  3
- comment 注释节点  8

#### 02.节点的名称和值
- childNodes:获取某个元素中的所有的子节点，使用中括号语法或者item()方法可以获取对应的节点
- nodeType：获取节点的类型
- nodeName：节点名称
- nodeValue：节点的值
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>节点</title>
</head>
<body>
<div id="box">
    <p>我是p标签</p>
    <span>hello</span>
    <i>i标签</i>
    <div>我是div</div>
    <!--<h3>h333</h3>-->
    <em>em标签</em>
</div>
<script>
    var oBox = document.getElementById("box");
    var nodes = oBox.childNodes;
    console.log(nodes);//节点的集合 NodeList类型
    console.log(nodes[3]);//直接可以获取到节点
    console.log(nodes.item(5));//直接可以获取到节点

    //document的节点类型 名称 和值
    console.log(document.nodeType);//9
    console.log(document.nodeName);//#document
    console.log(document.nodeValue);//null


    //元素节点的类型 名称和 值
    console.log(nodes[1].nodeType);//1
    console.log(nodes[1].nodeName);//节点名称就是标签名 大写
    console.log(nodes[1].nodeValue);//null

    //文本节点的类型 名称和 值
    console.log(nodes[0].nodeType);//3
    console.log(nodes[0].nodeName);//#text
    console.log(nodes[0].nodeValue);//当前的文本内容

    //注释节点的类型 名称和 值
    console.log(nodes[9].nodeType);//8
    console.log(nodes[9].nodeName);//#comment
    console.log(nodes[9].nodeValue);//当前被注释的内容

    var myAttr = document.createAttribute("my");
    myAttr.value = "yes";
    console.log(myAttr);
    console.log(myAttr.nodeType);//2
    console.log(myAttr.nodeName);//my  属性节点是标准的键值对形式   属性名就是节点名称
    console.log(myAttr.nodeValue);//yes  属性值就是节点的值

</script>
</body>
</html>
```
#### 03.节点关系
- DOM把文档视为一棵树形结构,也称为节点树。节点之间的关系包括:上下父子关
相邻兄弟关系
>在节点树中,最顶端节点为根节点。
除了根节点之外,每个节点都有一个父节点
节点可以包含任何数量的子节点
叶子是没有子节点的节点
同级节点是拥有相同父节点的节点

#### 04.访问节点
- parentNode 获取元素的父元素节点 (全兼容)
- children：获取元素的所有子元素节点(IE678 可以获取到注释节点 所有在IE678这样获取的时候注意不要写注释)

- previousSibling 获取元素的上一个兄弟节点（在ie678中获取的是上一个兄弟元素节点 在非ie678中获取的是上一个节点（可能是文本节点））
- previousElementSibling 在ie678中不支持 在非ie678中获取的是上一个元素节点（兼容性有顺序要求  previousSibling不能写前，因为previousSibling所有浏览器识别 但是意义不一样）

- nextSibling 获取下一个兄弟节点
- nextElementSibling 获取下一个兄弟节点

- firstChild:获取元素的第一个子元素节点
- firstElementChild:获取元素的第一个子元素节点

- lastChild:获取元素的最后一个子元素节点
- lastElementChild:获取元素的最后一个子元素节点

- <img src=https://upload-images.jianshu.io/upload_images/3532891-53a885d21fa868ea.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240>
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>访问元素节点</title>
</head>
<body>
<ul id="box">
    <li>11</li>
    <li>22</li>
    <li>33</li>
    <li>44</li>
<!--    <li>注释</li>-->
    <li>55</li>
</ul>
<div class="con">
    <div>1</div>
    <span>span</span>
    <p>p</p>
    <h2>h2</h2>
</div>
<script>

    //通过get选择器的方式选择
    var oBox = document.getElementById("box");
    var oLis = oBox.getElementsByTagName("li");
    console.log(oLis);

    /*var oCon = document.getElementsByClassName("con")[0];
    console.log(oCon.children);//  类数组集合 [div, span, p, h2]
    console.log(oBox.children);// 类数组集合  [li, li, li, li, li]*/

    //获取元素的父节点
    console.log(oLis[3]);
    console.log(oLis[3].parentNode);
    console.log(oLis[3].parentNode.parentNode);
    console.log(oLis[3].parentNode.parentNode.parentNode);
    console.log(oLis[3].parentNode.parentNode.parentNode.parentNode);
    console.log(oLis[3].parentNode.parentNode.parentNode.parentNode.parentNode);//null
    // console.log(oLis[3].parentNode.parentNode.parentNode.parentNode.parentNode.parentNode);//报错


    //获取上一个兄弟节点
    console.log(oLis[3].previousSibling);
    console.log(oLis[3].previousElementSibling);
    // 兼容性写法
    if (oLis[3].previousElementSibling){
        console.log(oLis[3].previousElementSibling);
    }else{
        console.log(oLis[3].previousSibling);
    }

    // 获取下一个兄弟
    console.log(oLis[3].nextElementSibling);

    //获取第一个子节点
    console.log(oBox.firstElementChild);

    //获取最后一个子节点
    console.log(oBox.lastElementChild);
</script>
</body>
</html>
```

### 04.节点操作
- 因为节点关系都是只读的，所以 DOM 提供了一些操作节点的方法
#### 01.创建节点
- 使用document对象的createElement方法能够根据参数指定的标签名创建一个新的元素。并返回对新元素的引用
- 使用creatElement方法创建的新元素不会被xz自动添加到文档里，需要使用appendChild等方法

#### 02.创建文本节点
- 使用document对象的createTextNode()方法可创建文本节点
- 参数是一个字符串
- 创建的文本节点需要使用appendChild等方法才能插入到元素节点中
- 当然也可以使用innerHTML方法给元素节点添加内容

#### 03.插入节点
##### 01.appendChild()
- appendChild()方法可以向当前节点的字节点列表的末尾添加新的节点
- 如果文档树中已经存在参数节点，则将从文档树中删除，然后重新插入新的位置

##### 02.insertBefore()
- 使用insertBefore(newChild,oldChild)方法可以在已有的子节点前插入一个新的子节点
- newChild表示新插入的节点，oldChild用于指定插入节点的后边的相邻位置。
- 插入成功以后，该方法返回新插入的节点
- insertBefore可以把指定元素及其所包含的所有子节点都一起插入到指定位置中。同时会先删除移动的元素，再重新插入

#### 04.复制节点
- cloneNode()方法可以创建一个节点的副本
- 参数 true (深复制)，复制整个节点和里面的内容zs； false (浅复制)，只复制节点不要里面的内容
- 复制后的新节点，也不会被自动插入到文档，需要用到之前的方法去插入
- 由于复制的节点会包含原节点的所有特性，如果原节点中包含id属性，就会出现id属性值重叠的情况。为了避免潜在的冲突，应修改其中某个节点的id属性值

#### 05.删除节点
- removeChild方法可以从子节点列表中删除某个节点
- 如果删除成功，则返回被删除的节点，如果失败则返回null
- 当remove 删除节点的时候，该节点所包含的所有子节点将同时被删除

#### 06.替换节点
- replaceChild(new,old)方法可以将某个子节点替换为另一个
- 替换节点替换的是所有子节点以及包含的所有内容
- 其中参数new为指定的新节点，old代表被替换的节点
- 如果替换成功则返回被替换的节点，否则返回null
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>节点的操作</title>
</head>
<body>
<button id="btn1">按钮1</button>
<button id="btn2">按钮2</button>
<button id="btn3">按钮3</button>
<button id="btn4">按钮4</button>
<button id="btn5">按钮5</button>
<button id="empty">清空</button>
<ul id="box">
    <li>11</li>
    <li>22</li>
    <li my = "hello">33</li>
    <li>44</li>
</ul>

<script>
    var oBox = document.getElementById("box");
    var oLis = oBox.getElementsByTagName("li");
    var oBtn1 = document.getElementById("btn1");
    var oBtn2 = document.getElementById("btn2");
    var oBtn3 = document.getElementById("btn3");
    var oBtn4 = document.getElementById("btn4");
    var oBtn5 = document.getElementById("btn5");
    var oEmpty = document.getElementById("empty");
    // 创建一个元素节点
    var newLi = document.createElement("li");
    console.log(newLi);

    //创建文本节点
    var newLiText = document.createTextNode("you 这谁呀 怎么这么帅");
    console.log(newLiText);

    //使用innerHTML给新节点传入内容
    newLi.innerHTML = "今天天气真好 <a herf='###' class='delete'>删除</a>";
    console.log(newLi);

    //给ul的尾部添加一个新的节点
    oBtn1.onclick = function(){
        // oBox.appendChild(newLiText);//插入文本节点
        newLi.appendChild(newLiText);//把文本节点插入新创建的li中
        oBox.appendChild(newLi);//直接插入元素节点

        var oDele = document.getElementsByClassName("delete")[0];
        console.log(oDele);
        oDele.onclick = function () {
            // console.log(oDele.parentNode.parentNode.removeChild(oDele.parentNode));;
            // remove(oDele.parentNode)
        }
    }

    //把已经存在的元素插入到某个元素的最后边
    oBtn2.onclick = function () {
        // oBox.appendChild(oLis[1]);
        console.log(oBox.appendChild(this));;//没有限制，只要获取到这个元素，就可以任意插入
    }

    //使用insertBefore插入节点
    oBtn3.onclick = function () {
        // console.log(oBox.insertBefore(newLi, oLis[1]));
        // console.log(oBox.insertBefore(oLis[3], oLis[1]));
        // prependChild(oBox,newLi)
        // insetAfter(newLi,oLis[1])
        // insetAfter(oLis[0],oLis[1])
        insetAfter(newLi,oLis[3]);
    }
    //克隆节点
    oBtn4.onclick = function () {
        console.log(oLis[2].cloneNode());
        console.log(oLis[2].cloneNode(true));
        console.log(oLis[2].cloneNode(false));
        /*var newClone = oLis[2].cloneNode(true);
        oBox.appendChild(newClone)*/
        oBox.appendChild(oLis[2].cloneNode(true));

    }
    //替换节点
    oBtn5.onclick = function () {
        console.log(oBox.replaceChild(newLi, oLis[2]));
        // console.log(document.documentElement.replaceChild(newLi, document.body));
    }

    oEmpty.onclick = function () {
        empty(oBox);
    }

    //在元素的最前边插入节点方法封装
    function prependChild(paren,ele) {
        if (paren.children.length) {
            paren.insertBefore(ele,paren.firstElementChild)
        }else{
            paren.appendChild(ele);
        }
        return ele;
    }
    //在某个节点的后边插入元素 方法封装
    function insetAfter(newele,oldele) {
        if (oldele.nextElementSibling){
            oldele.parentNode.insertBefore(newele,oldele.nextElementSibling);
        }else{
            oldele.parentNode.appendChild(newele);
        }
        return newele;
    }

    //封装函数，传入元素，将该元素在结构中删除
    function remove(ele) {
        if (ele){
            ele.parentNode.removeChild(ele);
            return ele
        }else{
            return undefined;
        }

    }

    //封装函数 传入参数，清空所有子节点
    function empty(ele) {
        while(ele.firstElementChild){
            ele.removeChild(ele.firstElementChild);
        }
    }

</script>
</body>
</html>
```


### 05.元素内容操作
#### 01.读取和插入HTML字符串
- 使用元素的innerHTML属性可以返回调用元素所包含的所有子节点对应的HTML标记的字符串
- 使用innerHTML属性可以根据传入的HTML字符串创建新的DOM片段
- 然后这个DOM片段完全替换调用元素原有的所有子节点
- 设置好innerHTML之后，就可以像访问文档中其他节点一样访问新创建的节点
- 使用documentElement和createTextNode方法创建长的结构，代码会非常长，而innerHTML会执行的更快
- 大多数浏览器，不支持执行innerHTML插入的script标签

#### 02.替换HTML字符串
- outerHTML和innerHTML的功能相同，但是它会包含元素自身。

#### 03.读写文本
- innerText 在指定的元素中插cc,s入文本，如果文本中包含HTML字符串，将被编码显示
- outerText功能和innerText功能相似，但是它能覆盖原有的元素。
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>元素内容的读取与写入</title>
</head>
<body>
    <button id="btn">按钮1</button>
    <button id="btn2">按钮2</button>
    <button id="btn3">按钮3</button>
    <ul id="box">
        <li>11</li>
        <li>22</li>
        <li>33</li>
        <li>44</li>
    </ul>
    <script>
        var oBtn = document.getElementById("btn");
        var oBtn2 = document.getElementById("btn2");
        var oBtn3 = document.getElementById("btn3");
        var oBox = document.getElementById("box");
        // 01.读取和插入html字符串--innerHTML
        oBtn.onclick = function () {
            // console.log(oBox.innerHTML);//把html也转成字符串输出

            // oBox.innerHTML = "<li>我是创建的li字符串 看我能不能被解析</li>"//替换原有所有内容

            var str = "<li>我是创建的li字符串 看我能不能被解析</li>";
            // oBox.appendChild(str);//appendChild插入字符串无效

            // oBox.innerHTML = oBox.innerHTML + str;

            oBox.innerHTML = str +oBox.innerHTML;
        }

        // 02.替换HTML字符串
        oBtn2.onclick = function () {
            // oBox.outerHTML = "<li>我是创建的li字符串 看我能不能被解析</li>";//包含box一起被替换了
            console.log(oBox.outerHTML);//包含box一起获取到了
        }

        oBtn3.onclick = function () {
            // oBox.innerText = "<li>我是创建的li字符串 看我能不能被解析</li>";
            // console.log(oBox.innerText);

            // console.log(oBox.outerText);
            oBox.outerText = "<li>我是创建的li字符串 看我能不能被解析</li>";
        }
    </script>
</body>
</html>
```

### 05.属性节点
#### 01.创建属性节点
- 使用document的createAttribute方法可以创建属性节点
- 使用属性节点的name属性，可以得到属性的名称
- 使用属性节点的value属性，可以设置和说去属性的值
- 创建的属性可以通过setAttribute来插入到元素中

#### 02.读取属性值
- 在传统的DOM中国，常用点语法通过元素直接访问HTML属性，如src、href等
- 但是还有很多属性没有支持，需要用规范的写法获取
- 使用getAttribute方法 可以读取指定属性的值
- 对于class属性，必须使用className属性名，因为class是JavaScript语言的保留字
- 对于for属性，则必须使用htmlFor属性名
- 补充，在脚本化css中设置float属性和text属性，要改为cssFloat和cssText（一次设置多个样式）使用

#### 03.设置属性值
- 使用元素的setAttribute(name,value)方法可以设置元素的属性值
- 参数name和value分别呆逼啊属性名称和属性值，并且必须是字符串
- 如果存在相同属性，则值被刷新，如果不存在则创建属性并添加

#### 04.删除属性
- 使用元素的removeAttribute()方法可以删除指定的属性
- 参数是要删除的属性名
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>属性的节点操作</title>
</head>
<body>
    <button id="btn1">按钮</button>
    <button id="btn2">按钮2</button>
    <ul id="box">
        <li>11</li>
        <li>22</li>
        <li>33</li>
        <li>44</li>
    </ul>
    <div id="con">
        <img src="./a.jpg" alt="我没有" your = "html" class="link">
        <a href="###">我是老A</a>
    </div>
    <script>
        var oCon = document.getElementById("con");
        var oBtn1 = document.getElementById("btn1");
        var oBtn2 = document.getElementById("btn2");
        oCons = oCon.children;

        // 1.创建属性节点
        var newAttr = document.createAttribute("my");
        console.log(newAttr.name);//获取属性节点的名
        console.log(newAttr.value);//获取属性节点的值
        newAttr.name = "your";//name属性这样设置无效
        newAttr.value = "js";//属性的值可以通过属性节点的value设置
        console.log(newAttr);

        //2.读取属性
        console.log(oCons[0].src);
        console.log(oCons[0].your);//不支持
        console.log(oCons[0].alt);
        console.log(oCons[1].href);

        console.log(oCons[0].class);

        console.log(oCons[0].getAttribute("your"));
        console.log(oCons[0].getAttribute("class"));


        //3.设置属性
        oBtn1.onclick = function () {
            oCons[0].alt = "我改变了";

            oCons[0].her = "hahah";//对于自定义属性来说，这样的方法是把标签当成了js对象，给对象扩展的属性和方法

            //如果想要给元素设置自定义属性， 就需要使用setAttribute方法

            oCons[1].setAttribute("his","jQuery");

            console.log(newAttr);

            oCons[0].setAttributeNode(newAttr);

        }

        oBtn2.onclick = function () {
            oCons[0].removeAttribute("your");
        }
    </script>
</body>
</html>
```

### 06.自定义属性
- HTML5允许用户为tdas元素自定义属性，但是要求添加前缀data-。
- 目的是为元素提供于渲染无关的附加信息，或者语义信息
- 可以使用dataset设置自定义属性名，不需要携带前缀
- 添加自定义属性后，可以通过元素的dataset属性访问自定义属性
- 删除自定义属性 可以使用delete方法
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>自定义属性</title>
</head>
<body>
<button id="btn">按钮</button>
<div id="box">
    <img src="./01.jpg" alt="图片">
    <span data-name="span">我是span</span>
</div>
<script>
    var oBox = document.getElementById("box");
    var oBtn = document.getElementById("btn");
    var oBoxs = oBox.children;

    oBtn.onclick = function () {
        console.log(oBoxs[1].getAttribute("data-name"));

        console.log(oBoxs[1].dataset);//自身是包含当前元素所有 data- 前缀的属性的集合对象
        oBoxs[1].dataset.sex = "不知道";

        delete oBoxs[1].dataset.name;
    }
</script>
</body>
</html>
```
### 07.文档片段节点
- DocumentFragment是一个虚拟的节点类型，仅仅存在于内存中，没有添加到文档树中，所以看不到渲染效果
- 使用文档碎片的好处，就是避免浏览器渲染和占用资源
- 当文档片段设计完善后，再使用js一次性添加到文档树中显示出来，提高效率，减少页面重绘的次数。解决大量添加节点时候的性能问题
- 使用document.createDocumentFragment()方法创建，使用appendChild等方法插入
```html
<!DOCTYPE html>d
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>插入节点的性能优化</title>
</head>
<body>
<ul id="box">

</ul>
<script>
    var oBox = document.getElementById("box");
    // 这种方法对DOM节点进行了100次的操作，非常耗费内存
    /*for (var i = 0; i < 100; i++) {
        var newLi = document.createElement("li");
        // textContent给元素插入文本
        newLi.textContent = "hello 6666";
        oBox.appendChild(newLi);
    }*/

    // createDocumentFragment创建一个DocumentFragment,它是一个轻量级的文档格式，作用是临时存储节点，等待插入到文档中
    // createDocumentFragment是解决大量添加节点时候的性能问题
    var fragment = document.createDocumentFragment();
    for (var i = 0; i < 100; i++) {
        var newLi = document.createElement("li");
        // textContent给元素插入文本
        newLi.textContent = "hello 6666";
        fragment.appendChild(newLi);
    }
    oBox.appendChild(fragment);
</script>
</body>
</html>
```

### 08.节点互换练习
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>节点互换练习</title>
    <link rel="stylesheet" href="./reset.css">
    <style>
        #outer{
            width: 700px;
            margin: 50px auto;
            border: 1px solid #000;
            overflow: hidden;
        }
        #con1{
            width: 300px;
            height: 400px;
            float: left;
            background-color: #4c71ff;
        }f
        #con2{
            width: 300px;
            height: 400px;
            float: right;
            background-color: #4c71ff;
        }
        #controls{
            width: 100px;
            height: 400px;
            float: left;
            background-color: #2ba5eb;
            text-align: center;
        }
        #con1 .red,#con2 .red{
            background-color: red;
        }
    </style>
</head>
<body>
    <div id="outer">
        <ul id="con1">
            <li>我是con1的内容1</li>
            <li>我是con1的内容2</li>
            <li>我是con1的内容3</li>
            <li>我是con1的内容4</li>
        </ul>
        <div id="controls">
            <button id="right">>>>>>>></button>
            <button id="left"><<<<<<<</button>
        </div>
        <ul id="con2">
            <li>我是con2的内容1</li>
            <li>我是con2的内容2</li>
            <li>我是con2的内容3</li>
            <li>我是con2的内容4</li>
        </ul>
    </div>
    <script>
        var oCon1 = document.getElementById("con1");
        var oCon2 = document.getElementById("con2");
        var oRight = document.getElementById("right");
        var oLeft = document.getElementById("left");
        var oCon1Lis = oCon1.getElementsByTagName("li");
        var oCon2Lis = oCon2.getElementsByTagName("li");

        // 给所有的oCon1中的li绑定点击事件，点击以后颜色发生变化，并且被选中
        for (var i = 0; i < oCon1Lis.length; i++) {
            oCon1Lis[i].onclick = function () {
                this.className = "red";
                // 我们给选中的元素一个标记（设置自定义属性 change=true）
                this.setAttribute("change","true");
            }
        }
        
        // 给oRight绑定点击事件 让选中的左边元素向右移动
        oRight.onclick = function () {
            //遍历所有的左边的li  判断哪一个被选中了
            for (var i = 0; i < oCon1Lis.length; i++) {
                // 判断哪一个li拥有change属性
                if (oCon1Lis[i].getAttribute("change")) {
                    //移动过去的元素 需要把颜色 自定义属性全部还原
                    oCon1Lis[i].className = "";
                    oCon1Lis[i].removeAttribute("change");

                    //把当前遍历的li给移动到oCon2中
                    oCon2.appendChild(oCon1Lis[i]);
                    // 因为移动过元素之后，后边的元素下标全部向上提一位，所以i要减1
                    i --;

                }
            }
        }

        // 给所有的oCon2中的li绑定点击事件，点击以后颜色发生变化，并且被选中
        for (var i = 0; i < oCon2Lis.length; i++) {
            oCon2Lis[i].onclick = function () {
                this.className = "red";
                // 我们给选中的元素一个标记（设置自定义属性 change=true）
                this.setAttribute("change","true");
            }
        }

        // 给oLeft绑定点击事件 让选中的右边元素向左移动
        oLeft.onclick = function () {
            //遍历所有的左边的li  判断哪一个被选中了
            for (var i = 0; i < oCon2Lis.length; i++) {
                // 判断哪一个li拥有change属性
                if (oCon2Lis[i].getAttribute("change")) {
                    //移动过去的元素 需要把颜色 自定义属性全部还原
                    oCon2Lis[i].className = "";
                    oCon2Lis[i].removeAttribute("change");

                    //把当前遍历的li给移动到oCon2中
                    oCon1.appendChild(oCon2Lis[i]);
                    // 因为移动过元素之后，后边的元素下标全部向上提一位，所以i要减1
                    i --;

                }
            }
        }
    </script>
</body>
</html>
```

### 09.css选择器获取节点
#### 01.核心方法
- selectors API就是由W3C发布的一个事实标准，为浏览器实现元素的css选择器
- 两个核心方法 querySelector和querySelectorAll（IE8+）
- querySelector和querySelectorAll方法参数必须是符合css选择器语法规则的字符串。其中querySelector返回的是一个元素，querySelectorAll返回的是一个集合。一个NodeList对象（可以使用数组的forEach方法）
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>新的选择器</title>
</head>
<body>
<ul class="outer">
    <li>11</li>
    <li>22</li>
    <li>33</li>
</ul>
<script>
    /*
    * w3c发布新的 seletors API  为浏览器js引擎实现css选择器选择元素
    *   两个核心的方法：querySelector（）   querySelectorAll（）
    *   两个方法接受的必须是 符合css选择器规范的字符串，其中querySelector返回的是一个元素，querySelectorAll返回的是一个集合（nodeList，可以使用数组的方法）
    *
    *   querySelector（） 选择符合条件的第一个元素节点
    *
    * */
    var oLis = document.querySelectorAll(".outer>li");
    console.log(oLis);//[li,li,li]
    console.log(oLis[0]);

    var oLi = document.querySelector(".outer>li");
    console.log(oLi);

    var oLi2 = document.querySelector(".outer>li:nth-child(2)");
    console.log(oLi2);
</script>
</body>
</html>
```

#### 02.getElementByXXXXX 和 queryselector的区别
- getElementsByXXXXX获取的是一个动态的集合
- queryselectorAll获取的是静态的集合
- 动态：选出来的元素会随着文档的改变而改变，静态：只要取出来，就和页面有没有任何关系
```js
    /*var oUl = document.getElementsByTagName("ul")[0];
    var oLis = oUl.getElementsByTagName("li");
    console.log(oLis.length);

    //直接陷入死循环  因为getElementsByTagName获取的元素是动态的，所以我们遍历的长度是获取元素的长度
    // 每次插入一个 长度就会加1  所有永远运行不完
    for (var i = 0; i < oLis.length; i++) {
        oUl.appendChild(document.createElement("li"))
    }
    console.log(oLis.length);*/



    // querySelectorAll获取的元素就是静态的
    var oLis = document.querySelectorAll("ul li");
    console.log(oLis.length);

    for (var i = 0; i < oLis.length; i++) {
        document.querySelector("ul").appendChild(document.createElement("li"))
    }
    console.log(oLis.length);
```

### 10.classList对象
- h5中新增了一个classList，原生js可以通过它来控制元素的类名。
- classList是html元素对象的成员，它的使用非常简单
- 目前已知classList API有length,item,add,remove,toggle,contains
- length静态属性。可以获取元素类名的个数
- item( Number )方法。可以获取元素的类名，接受一个参数，即数字索引
- add( )方法。可以给元素添加类名，就像jquery中的addClass()，它一次性只能增加一个类
- remove()方法。可以将元素的类名删除，一次只能删除一个类名
- toggle( )方法。可以给元素交替增加类名和删除类名
- contains()方法。可以检测判断元素是否包含某个类名，返回false或true
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>classList对象</title>
    <style>
        .con{
            width: 100px;
            height: 100px;
        }
        .show{
            background-color: yellow;
        }
        .red{
            color:red;
        }
        .blue{
            background-color: blue;
        }
    </style>
</head>
<body>
<button id="btn">按钮</button>
<div class="box">
    <p id="con" class="con show">concon</p>
</div>

<script>
    /*
    * html5为每一个元素新增了一个classList对象，classList对象保存着控制当前元素类名的各个方法和属性
    * - length 返回类名的个数
    * - add() 在原有的类名基础上添加一个类名
    * - remove() 在原有的类名基础上 移出某一个类名
    * - toggle() 如果有这个类名 则删除这个类名，如果没有 则添加减去
    * - item() 根据索引 获取类名
    * - contains()  判断元素是否包含某一个类名
    *
    * */
    var oBtn = document.getElementById("btn");
    var oCon = document.getElementById("con");

    oBtn.onclick = function () {
        // oCon.className = "red";
        // console.log(oCon.className);
        // oCon.className = "con show red";
        // oCon.className += " red";

        console.log(oCon.classList.length);

        oCon.classList.add("red");

        // oCon.classList.remove("con");

        oCon.classList.toggle("blue");

        console.log(oCon.classList.contains("con"));

        console.log(oCon.classList.item(0));
    }


</script>
</body>
</html>
```
## 十五、案例练习
### 01.侧边栏
#### 01.侧边栏单个版本
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>侧边栏基础版</title>
    <link rel="stylesheet" href="reset.css">
    <style>
        #box{
            position: fixed;
            right: 0;
            top: 200px;
        }
        #box li{
            position: relative;
            margin-bottom: 30px;
        }
        #box li span{
            width: 40px;
            height: 40px;
            font-size: 14px;
            line-height: 40px;
            text-align: center;
            background-color: #2ba5eb;
            display: block;
            color: #fff;
            position: relative;
            z-index: 2;
        }
        #box li p{
            width: 120px;
            height: 40px;
            line-height: 40px;
            text-align: center;
            position: absolute;
            left: 0;
            top: 0;
            background-color: indianred;
            color: #fff;
        }
    </style>
</head>
<body>
<ul id="box">
    <li>
        <span>反馈</span>
        <p>我的反馈</p>
    </li>
    <li>
        <span>反馈</span>
        <p>我的反馈</p>
    </li>
    <li>
        <span>反馈</span>
        <p>我的反馈</p>
    </li>
</ul>
<script>
    var oBox = document.getElementById("box");
    var oLis = oBox.getElementsByTagName("li");
    var oPs = oBox.getElementsByTagName("p");
    var oSpans = oBox.getElementsByTagName("span");
    var timer = null;
    var conLeft = 0;//定义一个变量  保存当前p标签的left值
    
    oLis[0].onmouseenter = function () {
        clearInterval(timer);
        timer = setInterval(function () {
            conLeft --;
            if (conLeft <= -120){
                conLeft = -120;
                clearInterval(timer);
            }
            oPs[0].style.left = conLeft + "px";
        },1)
    }

    oLis[0].onmouseleave = function () {
        clearInterval(timer);
        timer = setInterval(function () {
            conLeft ++;
            if (conLeft >= 0){
                conLeft = 0;
                clearInterval(timer);
            }
            oPs[0].style.left = conLeft + "px";
        },1)
    }
</script>
</body>
</html>
```

#### 02.侧边栏完整错误版
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>侧边栏完整版</title>
    <link rel="stylesheet" href="reset.css">
    <style>
        #box{
            position: fixed;
            right: 0;
            top: 200px;
        }
        #box li{
            position: relative;
            margin-bottom: 30px;
        }
        #box li span{
            width: 40px;
            height: 40px;
            font-size: 14px;
            line-height: 40px;
            text-align: center;
            background-color: #2ba5eb;
            display: block;
            color: #fff;
            position: relative;
            z-index: 2;
        }
        #box li p{
            width: 120px;
            height: 40px;
            line-height: 40px;
            text-align: center;
            position: absolute;
            left: 0;
            top: 0;
            background-color: indianred;
            color: #fff;
        }
    </style>
</head>
<body>
<ul id="box">
    <li>
        <span>反馈</span>
        <p>我的反馈</p>
    </li>
    <li>
        <span>反馈</span>
        <p>我的反馈</p>
    </li>
    <li>
        <span>反馈</span>
        <p>我的反馈</p>
    </li>
</ul>
<script>
    var oBox = document.getElementById("box");
    var oLis = oBox.getElementsByTagName("li");
    var oPs = oBox.getElementsByTagName("p");
    var oSpans = oBox.getElementsByTagName("span");

    //所有效果共用了一个 conLeft和一个timer  想要达到各自使用各自的  需要再嵌套一个函数
    var timer = null;
    var conLeft = 0;//定义一个变量  保存当前p标签的left值
    for (var i = 0; i < oLis.length; i++) {
        oLis[i].index = i;
        oLis[i].onmouseenter = function () {
            clearInterval(timer);
            var _this = this;//定义一个变量保存当前的this
            timer = setInterval(function () {
                conLeft --;
                if (conLeft <= -120){
                    conLeft = -120;
                    clearInterval(timer);
                }
                oPs[_this.index].style.left = conLeft + "px";
            },1)
        }

        oLis[i].onmouseleave = function () {
            clearInterval(timer);
            var _this = this;
            timer = setInterval(function () {
                conLeft ++;
                if (conLeft >= 0){
                    conLeft = 0;
                    clearInterval(timer);
                }
                oPs[_this.index].style.left = conLeft + "px";
            },1)
        }
    }


</script>
</body>
</html>
```

#### 03.侧边栏正确版本zh
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>侧边栏完整版</title>
    <link rel="stylesheet" href="reset.css">
    <style>
        #box{
            position: fixed;
            right: 0;
            top: 200px;
        }
        #box li{
            position: relative;
            margin-bottom: 30px;
        }
        #box li span{
            width: 40px;
            height: 40px;
            font-size: 14px;
            line-height: 40px;
            text-align: center;
            background-color: #2ba5eb;
            display: block;
            color: #fff;
            position: relative;
            z-index: 2;
        }
        #box li p{
            width: 120px;
            height: 40px;
            line-height: 40px;
            text-align: center;
            position: absolute;
            left: 0;
            top: 0;
            background-color: indianred;
            color: #fff;
        }
    </style>
</head>
<body>
<ul id="box">
    <li>
        <span>反馈</span>
        <p>我的反馈</p>
    </li>
    <li>
        <span>反馈</span>
        <p>我的反馈</p>
    </li>
    <li>
        <span>反馈</span>
        <p>我的反馈</p>
    </li>
</ul>
<script>
    var oBox = document.getElementById("box");
    var oLis = oBox.getElementsByTagName("li");
    var oPs = oBox.getElementsByTagName("p");
    var oSpans = oBox.getElementsByTagName("span");


    function fn1(i) {
        var timer = null;
        var conLeft = 0;//定义一个变量  保存当前p标签的left值
        oLis[i].index = i;
        oLis[i].onmouseenter = function () {
            clearInterval(timer);
            var _this = this;//定义一个变量保存当前的this
            timer = setInterval(function () {
                conLeft --;
                if (conLeft <= -120){
                    conLeft = -120;
                    clearInterval(timer);
                }
                oPs[_this.index].style.left = conLeft + "px";
            },1)
        }

        oLis[i].onmouseleave = function () {
            clearInterval(timer);
            var _this = this;
            timer = setInterval(function () {
                conLeft ++;
                if (conLeft >= 0){
                    conLeft = 0;
                    clearInterval(timer);
                }
                oPs[_this.index].style.left = conLeft + "px";
            },1)
        }
    }

    for (var i = 0; i < oLis.length; i++) {
        fn1(i);
    }

</script>
</body>
</html>
```

### 02.Tab切换动画版
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>tab切换动画版</title>
    <link rel="stylesheet" href="./reset.css">
    <style>
        .outer{
            width: 608px;
            margin: 0 auto;
            border: 1px solid #000;
        }
        #title{
            overflow: hidden;
        }
        #title h2{
            width: 150px;
            border: 1px solid red;
            float: left;
            height: 40px;
            font-size: 20px;
            line-height: 40px;
            text-align: center;
            color: #fff;
            background-color: #ccc;
            cursor: pointer;
        }
        #title .active{
            background-color: red;
        }
        #con{
            height: 350px;
            /*overflow-y: scroll;*/
            overflow: hidden;
        }
        #con li{
            height: 350px;
        }
        #con li img{
            width: 608px;
            height: 350px;
            display: block;
        }
    </style>
</head>
<body>
    <div class="outer">
        <div id="title">
            <h2 class="active">科技潮品</h2>
            <h2>司法拍卖</h2>
            <h2>爱逛街</h2>
            <h2>游戏动漫</h2>
        </div>
        <ul id="con">
            <li class="show"><img src="../images/01.png" alt=""></li>
            <li><img src="../images/02.png" alt=""></li>
            <li><img src="../images/03.png" alt=""></li>
            <li><img src="../images/04.png" alt=""></li>
        </ul>
    </div>
    <script>
        var oTitle = document.getElementById("title");
        var oCon = document.getElementById("con");
        var oH2s = oTitle.getElementsByTagName("h2");
        var oLis = oCon.getElementsByTagName("li");
        var timer = null;
        for (var i = 0; i < oH2s.length; i++) {
            oH2s[i].onclick = function () {
                clearInterval(timer);
                for (var j = 0; j < oH2s.length; j++) {
                    if (oH2s[j] == this){
                        oH2s[j].className = "active";
                        //获取起始位置
                        var start = oCon.scrollTop;
                        //获取结束位置
                        var end = j * oLis[0].offsetHeight;
                        //设置起始步数
                        var startStep = 0;
                        //设置总步数
                        var endStep = 40;
                        //计算每一步所走的距离
                        var everyStep = (end - start) / (endStep - startStep);
                        //进入计时器  让计时器每次运行都走 everyStep的距离  总共走endStep次 就可以执行完

                        timer = setInterval(function () {
                            // 每次进入计时器 让startStep++  用来保存执行次数
                            startStep ++;
                            // 临界值 当startStep等于endStep  那么说明运动完成
                            if (startStep >= endStep){
                                startStep = 0;
                                clearInterval(timer);
                            }
                            start += everyStep;
                            oCon.scrollTop = start;
                        },10)

                    }else{
                        oH2s[j].className = "";
                    }
                }
            }
        }
    </script>
</body>
</html>s
```

## 十六、Math对象
- Math对象是JavaScript的内置对象，提供一系列的数学常数和数学方法。Math对象只提供了静态的属性和方法，所以使用时，不需要实例化。
### 00.JS对象的分类：
#### 01.内部对象：
- js中的内部对象包括Array、Boolean、Date、Function、Global、Math、Number、Object、RegExp、String以及各种错误类对象，包括Error、EvalError、RangeError、ReferenceError、SyntaxError和TypeError。
- 其中Global和Math这两个对象又被称为“内置对象”，这两个对象在脚本程序初始化时被创建，不必实例化这两个对象。

#### 02.宿主对象
- 宿主对象就是执行JS脚本的环境提供的对象。对于嵌入到网页中的JS来说，其宿主对象就是浏览器提供的对象，所以又称为浏览器对象，如IE、Firefox等浏览器提供的对象。不同的浏览器提供的宿主对象可能不同，即使提供的对象相同，其实现方式也大相径庭！这会带来浏览器兼容问题，增加开发难度。
浏览器对象有很多，如Window和Document，Element，form，image，等等。

#### 03.自定义对象
- 顾名思义，就是开发人员自己定义的对象。JS允许使用自定义对象，使JS应用及功能得到扩充


### 01.Math对象的属性
- Math对象提供以下一些只读的数学常数。
- Math.E // 2.718281828459045（自然底数 无限不循环小数）lim(1+1/n)^n=e  ,n→+∞
- Math.LN2 // 0.6931471805599453（2的自然对数）
- Math.LN10 // 2.302585092994046（10的自然对数）
- Math.LOG2E // 1.4426950408889634（2为底 e的对数）
- Math.LOG10E // 0.4342944819032518
- Math.PI // 3.141592653589793
- Math.SQRT1_2 // 0.7071067811865476
- Math.SQRT2 // 1.4142135623730951
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Math对象的属性</title>
</head>
<body>
<h2>请输入你家花园的半径 单位是m</h2>
<input type="text" id="ipt">
<h2>你家花园的面积是 <span id="area"></span>，  你家花园的周长是 <span id="length"></span></h2>
<script>
    // 获取π
    console.log(Math.PI);
    //获取自然底数
    console.log(Math.E);
    //获取2的和1/2平方根
    console.log(Math.SQRT2);
    console.log(Math.SQRT1_2);

    // 练习
    var oIpt = document.getElementById("ipt");
    var oArea = document.getElementById("area");
    var oLength = document.getElementById("length");
    oIpt.onchange = function () {
        oArea.innerHTML = Math.PI * oIpt.value * oIpt.value;
        oLength.innerHTML = 2 * Math.PI * oIpt.value;
    }
</script>
</body>
</html>
```

### 02.Math对象的方法
- Math.abs()：求绝对值 对一个数字进行绝对值操作，并且也能对纯数字的字符串操作
- Math.ceil():向上取整 向大的数值取整
- Math.floor():向下取整 向小的数值取整
- Math.round():四舍五入,四舍五入是对小数点的后一位进行判断
    正数的时候，当小数点后一位大于等于5的时候  整数部分加1  小于5的时候  整数部分不变
    负数的时候  当小数点后一位 大于5的时候 整数减1  小于5的时候 整数不变
    负数的时候 当小数点后一位是5 后边没有第二个小数位了  整数不变；如果5后还有小数位 那么 整数减1
- Math.min()和Math.max() 计算一组数值中的最大值和最小值
- pow:返回以第一个参数为底数，第二个参数为幂的指数值
- sqrt： 返回参数的平方根，如果参数是负数，返回NaN
- sin cos tan
- Math.random():求随机数 生成 [0,1) （大于等于0  小于1） 小数随机数
```js

    console.log(Math.abs(4));;//4
    console.log(Math.abs(-4));;//4
    console.log(Math.abs(-Infinity));;//Infinity
    console.log(Math.abs("-3px"));;//NaN
    console.log(Math.abs("-3"));;//3


    console.log(Math.ceil(3.1));//4
    console.log(Math.ceil(3.5));//4
    console.log(Math.ceil(-3.1));//-3
    console.log(Math.ceil(-3.5));//-3

    console.log(Math.floor(3.1));//3
    console.log(Math.floor(3.5));//3
    console.log(Math.floor(-3.1));//-4
    console.log(Math.floor(-3.5));//-4

    console.log(Math.round(3.1));;//3
    console.log(Math.round(3.5));;//4
    console.log(Math.round(3.55));;//4
    console.log(Math.round(3.6));;//4
    console.log(Math.round(-3.1));;//-3
    console.log(Math.round(-3.5));;//-3
    console.log(Math.round(-3.51));;//-4
    console.log(Math.round(-3.6));;//-4


    console.log(Math.max(45, 32, 45, 65, 12, 3, 8, 45, 33));
    console.log(Math.min(45, 32, 45, 65, 12, 3, 8, 45, 33));

    console.log(Math.pow(2, 200));
    console.log(Math.pow(2.1, 200));

    // 1度的弧度 ：2 * Math.PI / 360
    console.log(Math.sin(30 * 2 * Math.PI / 360));

    console.log(Math.sqrt(4));

    setInterval(function () {
        console.log(Math.random());
    },300)
```
```js
//得到[a,b)的随机数
function random(a,b) {
 return a + Math.floor(Math.random()*(b-a));
}

// 得到一个随机字符串
function randomStr(len){
    var dict = '0123456789abcdefghigklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ'
    var str = '';
    for(var i = 0; i < len; i ++){
        str += dict[random(0,62)]//获取数组的下表所对应的元素
    }
    return str;
}

//如何得到一个随机的IP地址：0.0.0.0~255.255.255.255
function randomIP(len){
    var arr = []
    for(var i = 0; i < 4; i++){
        arr.push(random(0,256));
    }
    return arr.join('.');
}

//有一半的几率在做什么事情，另一半的几率在做另一件事
if(Math.random() > 0.5){
    console.log('haha');
}else{
    console.log('ninini');
}
```
### 03.小球曲线运动
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>小球曲线运动</title>
    <style>
        #box{
            width: 20px;
            height: 20px;
            background-color: red;
            border-radius: 50%;

            position: fixed;
            left: 20px;
            top: 300px;
        }
    </style>
</head>
<body>
    <div id="box">

    </div>
    <script>
        var oBox = document.getElementById("box");
        var timer = null;
        var degStart = 0;
        timer = setInterval(function () {
            degStart ++;
            oBox.style.left = 20 + degStart + "px";
            oBox.style.top = 300 + Math.sin(degStart * 2 * Math.PI / 360)*100 + "px";
        },10)
    </script>
</body>
</html>
```

### 04.小球曲线运动路径版
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>小球曲线运动</title>
    <style>
        #box{
            width: 20px;
            height: 20px;
            background-color: red;
            border-radius: 50%;

            position: fixed;
            left: 20px;
            top: 300px;
        }
        .show{
            width: 20px;
            height: 20px;
            background-color: red;
            border-radius: 50%;
            position: fixed;
        }
    </style>
</head>
<body>
    <div id="box">

    </div>
    <script>
        var oBox = document.getElementById("box");
        var timer = null;
        var degStart = 0;
        timer = setInterval(function () {
            var newBox = document.createElement("div");
            newBox.className = "show";
            document.body.appendChild(newBox);
            degStart ++;
            newBox.style.left = 20 + degStart + "px";
            // newBox.style.top = 300 + Math.sin(degStart * 2 * Math.PI / 360)*100 + "px";
            // newBox.style.top = 300 + -Math.abs(Math.sin(degStart * 2 * Math.PI / 360)*100) + "px";
            newBox.style.top = 300 + -(Math.sin(degStart * 2 * Math.PI / 360)*100) + "px";
        },10)
    </script>
</body>
</html>
```

### 05.点名器
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>点名器</title>
    <style>
        body{
            background-color: #0D1635;
        }
        h2{
            font-size: 70px;
            color: yellow;
            text-align: center;
        }
        p{
            font-size: 60px;
            color: #fff;
            text-align: center;
        }
    </style>
</head>
<body>
    <h2 id="btn">start</h2>
    <p id="con">开始点名</p>
    <script>
        var oBtn = document.getElementById("btn");
        var oCon = document.getElementById("con");
        var names = ["陈纪法","张三","李四","胡宝林","柏洪洋"];
        var flag = true;//保存当前停止状态
        var timer = null;
        oBtn.onclick = function () {
            if(flag){
                oBtn.innerHTML = "stop";
                timer = setInterval(function () {
                    // names中的值应该是[0,4]  [0,5)
                    oCon.innerHTML = names[Math.floor(Math.random()*names.length)];
                },30)
            }else{
                oBtn.innerHTML = "start";
                clearInterval(timer);
            }

            flag = !flag;
        }
    </script>
</body>
</html>
```


## 十七、时间对象
### 01.获取时间
- Date用来处理日期和时间的
```js
    // 获取当前的时间
    var now = new Date();
    console.log(now)//Fri Aug 02 2019 14:20:09 GMT+0800 (伊尔库茨克标准时间)
    console.log(typeof now)//对象
```
### 02.创建一个时间 new Date(指定时间)
- 传入一个毫秒数（会把毫秒数转换成一个时间c  然后加上1970年1月1日 8：00 的时间）
- 传入一个字符串格式的时间  2028-10-2 10:10:29
- 传入多个参数 分别代表年 月 日 时 分 秒 毫秒
```js
    var date1 = new Date(1000 * 60 * 60);
    var date1 = new Date(1546354578234);
    console.log(date1);

    var date2 = new Date("2019-10-01 8:0:0");
    var date2 = new Date("2019-10-1");//如果不写时间 只写年月日 那么时间按照00点来计算
    var date2 = new Date("8:0:0");//Invalid Date 如果不写年月日 那么时间是错误的
    console.log(date2);

    var date3 = new Date(2019,9,1,8,10,20,300);//当数字形式传递或者获取月份的时候，月份是从0开始算  0 代表 1月
    var date3 = new Date(2019,16,1,8,10,20,300);//时间超出分为 会自动向前进一位  但是不建议这么写
    console.log(date3);
```

### 03.获取时间
- 时间对象 无论是当前的时间还是我们设置的时间 都拥有获取精确年月日等等单独时间的方法
- 获取年份 getFullYear
- 获取月份 getMonth
- 获取日 getDate
- 获取小时 getHours
- 获取分钟 getMinutes
- 获取秒 getSeconds
- 获取毫秒 getMilliseconds
- 获取星期 getDay
- 获取当前距离1970年1月1日8:00:00 的毫秒数  getTime
```js
    var now = new Date();

    //获取年份
    var nowYear = now.getFullYear();
    // var nowYear = now.getYear();//只获取后两位  2000年之前的方法。我们不推荐使用
    console.log(nowYear);//2019
    console.log(typeof nowYear);//number

    //获取月份
    var nowMonth = now.getMonth();
    console.log(nowMonth);//7  代表8月  月份从0开始计算

    //获取日
    var nowDate = now.getDate();
    console.log(nowDate);//2

    // 获取小时
    var nowHours = now.getHours();
    console.log(nowHours);//24小时时间

    //获取分钟
    var nowMinutes = now.getMinutes();
    console.log(nowMinutes);//42

    // 获取秒
    var nowseconds = now.getSeconds();
    console.log(nowseconds)//11

    //获取毫秒
    var nowMilliseconds = now.getMilliseconds();
    console.log(nowMilliseconds);

    // 获取星期
    var nowDay = now.getDay();
    console.log(nowDay);//5

    //获取当前距离1970年1月1日8:00:00 的毫秒数
    var nowTime = now.getTime();
    console.log(nowTime);
```
### 04.北京时间练习
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>北京时间练习</title>
</head>
<body>
<div id="time">
<!--    当前时间是 2019 年 08 月 02 日 14 时 46 分 40秒 018毫秒-->

</div>
<script>
    var oTime = document.getElementById("time");
    //给 月 日 时 分 秒 添加0的函数
    function addZero(n) {
        return n>10 ? n : "0"+n;
    }
    function getNowTime() {
        var now = new Date();

        var y = now.getFullYear();

        var m = now.getMonth() + 1;
        m = addZero(m);

        var d = now.getDate();
        d = addZero(d);

        var h = now.getHours();
        h = addZero(h);

        var min = now.getMinutes();
        min = addZero(min);

        var s = now.getSeconds();
        s = addZero(s);

        var mili = now.getMilliseconds();
        if (mili < 10){
            mili = "00" + mili;
        } else if (mili<100){
            mili = "0" + mili;
        }

        var nowTime = y + "年" + m + "月" + d + "日" + h + "时" + min + "分" + s + "秒" + mili + "毫秒"
        oTime.innerHTML = nowTime;
    }

    var timer = setInterval(getNowTime,1);
</script>
</body>
</html>
```

### 05.设置单独的时间
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>设置时间</title>
</head>
<body>
<script>
    var now = new Date();

    //设置年份
    now.setFullYear(2023);
    console.log(now);

    //设置月份
    now.setMonth(0);
    console.log(now);

    //设置日期
    now.setDate(4);
    console.log(now);

    //设置 小时
    now.setHours(19);
    console.log(now);

    //设置分钟
    now.setMinutes(40);
    console.log(now);

    //设置秒
    now.setSeconds(10);
    console.log(now);

    //设置毫秒
    now.setMilliseconds(100);
    console.log(now)

    //设置星期  不允许 没有这个方法
    now.setDay();
    console.log(now);
</script>
</body>
</html>
```




















### 06.设置时间练习
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>设置时间练习</title>
</head>
<body>
<script>
    //设置一个3天后的当前时间
   /* //获取当前时间
    var now = new Date();
    //获取当前时间的日期
    var nowDate = now.getDate();
    //让当前的日期 加上3
    newDate = nowDate+3;

    // 获取一个当前的时间，然后把当前时间的日期 设置为newDate
    // console.log(newDate)
    var newTime = new Date();
    newTime = newTime.setDate(newDate);
    console.log(newTime);*/


    var threeDatLast = new Date();
    threeDatLast.setDate(new Date().getDate()+3);
    console.log(threeDatLast.toLocaleString());
</script>
</body>
</html>
```

### 07.获取时间戳
- 时间戳：1970年1月1日 8点距离现在的毫秒数
```js
    // 获取时间戳
    //方法1:  通过getTime（）
    /*var now = new Date();
    var time = now.getTime();
    console.log(time);*/

    // 方法二 将时间对象转换成数字   Number  一元运算
    var now = new Date();
    /*var time = Numb er(now);
    console.log(time);*/

    /*var time = + now;
    console.log(time);*/

    /*var time = parseInt(now);//parseInt不能转
    console.log(time);*/

    //方法三  valueOf 返回当前对象的最原始的值
    /*var time = now.valueOf();
    console.log(time);*/

    //方法四 Date对象 不用实例化  直接拥有一个now方法  返回当前的毫秒数
    var time = Date.now();
    console.log(time);
```

### 08.计算代码运行时间1
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>计算代码运行时间</title>
</head>
<body>
<script>
    var start = new Date();

    var num = 0;
    for (var i = 0; i < 100000000; i++) {
        num += i;
    }

    var end = new Date();

    // 两个时间对象相减 可以直接得到毫秒数
    console.log(end - start);
</script>
</body>
</html>
```

### 08.计算代码运行时间2
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>计算代码运行时间</title>
</head>
<body>
<script>
    console.time("name");
    var num = 0; 
    for (var i = 0; i < 100000000; i++) {
        num += i;
    }
    console.timeEnd("name");

    /* console.time() 中需要传递一个参数 代表当前计算时间的代号
     console.timeEnd() 中需要传递一个参数 查找相同参数的 time   然后计算出来之间的差值时间  并打印*/
</script>
</body>
</html>
```

### 09.倒计时
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>倒计时</title>
</head>
<body>
<div id="con">

</div>
<script>

    function fn1() {
        //获取距离国庆节还有多少时间
        var guoqing = new Date(2019,9,1,8,0,0);//国庆节时间
        var now = new Date();//当前时间
        var reduceTime = guoqing - now;//距离国庆假还有多少毫秒数
        // console.log(reduceTime)h;

        // 获取天
        var date = parseInt(reduceTime / (1000 * 60 * 60 * 24));
        date < 10 ? date = "0" + date : date;

        // 获取小时
        var _date = reduceTime % (1000 * 60 * 60 * 24);
        var hours =parseInt( _date / (1000 * 60 * 60 ));
        hours < 10 ? hours = "0" + hours : hours;


        // 获取分钟
        var _hours = _date % (1000 * 60 * 60);
        var minu =parseInt( _hours / (1000 * 60 ));
        minu < 10 ? minu = "0" + minu : minu;

        // 获取秒
        var _minu = _hours % (1000 * 60);
        var sec =parseInt( _minu / (1000 ));
        sec < 10 ? sec = "0" + sec : sec;

        var str = "距离国庆假还有" + date + "天" + hours + "小时" + minu + "分" + sec + "秒";
        document.getElementById("con").innerHTML = str;
    }
    setInterval(fn1,1000);
</script>
</body>
</html>
```
## 十八、字符串方法
### 01.concat方法
- 使用字符串的concat的方法可以把多个参数添加到指定字符串的尾部
- 参数类型和个数没有限制，把所有参数转换为字符串，返回连接以后的字符串fd
- 特定情况下，可以使用加法 和 数组的join 拼接字符串
- 原本数组的join方法代替concat方法，速度很快。但是当代浏览器优化加号拼接。所以推荐使用加号拼接
```js
    var str = "hello";
    var _str = str.concat("world","oh");
    console.log(str);//hello
    console.log(_str);//helloworldoh


    var str2 = "hello";
    var _str2 = str.concat("world",['oh','nice'],{name:"laowang"});
    console.log(str2);//hello
    console.log(_str2);//helloworldoh,nice[object Object]


    var straLL = "0123456789abcdefghijklmnopqrstuvwxyz";
    var strArr = [];
    for (var i = 0; i < 20; i++) {
        var strNum = Math.floor(Math.random() * straLL.length)
        strArr.push(straLL[strNum]);
    }
    var finallyStr = strArr.join("");
    console.log(finallyStr);
```

### 02.字符串查找
- charAt(n) 返回字符串中的第n个字符，参数如果不是0 --- length-1 之间，则返回空字符串
- indexOf和lastIndexOf：可以根据参数字符串，返回指定子字符串的下标位置。
    两个方法都有两个参数，第一个参数查找的目标，第二个参数是起始位置
- search 方法于indexOf的功能是相同的，查找指定字符串第一次出现的位置，但是只有一个参数，定义匹配模式，没有反向检索和全局模式。
- macth方法能够找出所有匹配的子字符串，并以数组的形式返回，如果匹配模式没有指定全局，则进行1次匹配。如果没找到则返回null
```js
// 01.charAt
    var str = "hello i am fine thankyou";
    console.log(str.charAt(8));//a
    console.log(str.charAt(0));//a
    console.log(str.charAt(str.length));//空字符串

    //02.indexOf()和lastIndexOf()
    var str = "hello i am fine thankyou";
    console.log(str.indexOf("a"));//8
    console.log(str.lastIndexOf("a"));//18
    console.log(str.indexOf("a",9));//18
    console.log(str.lastIndexOf("a",5));//-1  倒着查  5是下标

    // 03.search();
    var str = "110p1101h110";
    var index1 = str.search(/[a-zA-Z]/g);
    console.log(index1);

    // 04.match()
    var str = "110p1101h110";
    var index2 = str.match(/[a-zA-Z]/g);
    console.log(index2);//["p","h"]
```

### 03.字符串截取
- substr方法：substr能够根据指定长度来截取子字符串。包含两个参数，一个是起始下标，一个是截取的长度。省略第二个参数则代表末尾（ECMA不再推荐该方法）
- slice和substring方法都是根据指定的起止下标来截取字符串的，包含两个参数，一个是开始下标，一个是结束下标（不包含），第二个参数省略则代表末尾
- 起始和结束位置相比较的大小无法确定的时候可以使用substring。
- 如果为负值，slice能把负值当作从右向左。而substring视其无效
```js
    var str = "today is a fine day";
    var _str = str.substr(4,5);
    console.log(str);//today is a fine day
    console.log(_str);//y is
    var _str = str.substr(4);
    console.log(_str);//y is a fine day


    var str2 = "today is a fine day";
    var _str2 = str2.substring(4,8);
    console.log(str2);//today is a fine day
    console.log(_str2);//y is
    var _str2 = str2.substring(4);
    console.log(_str2);//y is a fine day

    var str3 = "today is a fine day";
    var _str3 = str3.slice(4,8);
    console.log(str3);//today is a fine day
    console.log(_str3);//y is
    var _str3 = str3.slice(4);
    console.log(_str3);//y is a fine day


    var str3 = "today is a fine day";
    var _str3 = str3.slice(4,-11);
    console.log(str3);//today is a fine day
    console.log(_str3);//y is a

    var str2 = "today is a fine day";
    var _str2 = str2.substring(4,-1);
    console.log(str2);//today is a fine day
    console.log(_str2);//toda
```

### 04.字符串大小转换
- toLowerCase():将字符串转换成小写
- toUpperCase():将字符串转换成大写
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>字符串的大小写转换</title>
    <style>
        #ipt{
            width: 200px;
            height: 50px;
            border: 1px solid red;
        }
    </style>
</head>
<body>
<div id="outer">
    请输入验证码：
    <input type="text" id="ipt">
    <button id="con">hj76tr</button>
</div>
<script>
    /*
    *   toLowerCase() 转成小写字母
    *   toUpperCase() 转成大写字母
    * */
    var oCon = document.getElementById("con");
    var oIpt = document.getElementById("ipt");

    oIpt.onchange = function () {
        if (oIpt.value.toLowerCase() === oCon.innerHTML) {
            oIpt.style.borderColor = "green";
        }
    }
</script>
</body>
</html>
```

### 05.字符串与数组转换
- 使用字符串的split方法可以根据指定的分割符把字符串切分成数组
- 如果参数是空字符串，则按照单个字符切分，返回和字符串等长的数组
- 如果没有参数，则把字符串当作返回数组的一个值
- 支持第二个参数，代表数组的最大长度
```js
    var str = "哎,呦,不,错,哦";
    var arr = str.split();
    var arr2 = str.split('');
    var arr3 = str.split(',');
    var arr4 = str.split(',',3);
    console.log(str);
    console.log(arr);//["哎,呦,不,错,哦"]
    console.log(arr2);// ["哎", ",", "呦", ",", "不", ",", "错", ",", "哦"]
    console.log(arr3);//["哎", "呦", "不", "错", "哦"]
    console.log(arr4);// ["哎", "呦", "不"]
```

### 06.清除两侧空字符串
- ES5新增了trim方法，用以从字符串中移除前导空字符和尾部空字符和行行终止符
- 常用在表单
```js
    var str1 = "   kajsbd  asknj df asf adf  \n";
    console.log(str1.trim());
```

### 07.将字符串转换成对象
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>将字符串转换成对象</title>
</head>
<body>
<script>
    // http://www.baidu.com?username=xiaowang&password=12345&age=18&sex=女&score=90
    // {username:"xiaowang",password:12345,age:18,sex:"女",score:90}

    var url = "http://www.baidu.com?username=xiaowang&password=12345&age=18&sex=女&score=90";
    var obj = {};
    var strArr = url.split("?");
    // console.log(strArr[1]);//username=xiaowang&password=12345&age=18&sex=女&score=90
    var strArr2 = strArr[1].split("&");
    // console.log(strArr2);//["username=xiaowang", "password=12345", "age=18", "sex=女", "score=90"]
    for (var i = 0; i < strArr2.length; i++) {
        // strArr2[i].split("=")//["username","xiaowang"]
        obj[strArr2[i].split("=")[0]] = strArr2[i].split("=")[1];
    }
    console.log(obj);//{username: "xiaowang", password: "12345", age: "18", sex: "女", score: "90"}



    // var str = 'username=xiaowang&password=12345&age=18&sex=女&score=90'
    function queryString(str) {
        var obj = {};
        var strArr2 = str.split("&");
        for (var i = 0; i < strArr2.length; i++) {
            obj [ strArr2[i].split("=")[0] ] = strArr2[i].split("=")[1];
        }
        return obj;
    }
</script>
</body>
</html>
```
### 08.对象转字符串
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>将对象转换成字符串</title>
</head>
<body>
<script>
    // 已知我们得到的对象是：{username: "xiaowang", password: "12345", age: "18", sex: "女", score: "90"}
    // 已知被拼接的url地址是：http://www.baidu.com
    // 最终得到：http://www.baidu.com?username=xiaowang&password=12345&age=18&sex=女&score=90

    var obj = {username: "xiaowang", password: "12345", age: "18", sex: "女", score: "90"};
    var url = "http://www.baidu.com";

    // 第一个目标：["username=xiaowang", "password=12345", "age=18", "sex=女", "score=90"]
    var arr = [];
    for(var i in obj){
        var str = i + "=" + obj[i];
        // console.log(str);//username=xiaowang
        arr.push(str);
    }
    // console.log(arr); //["username=xiaowang", "password=12345", "age=18", "sex=女", "score=90"]

    // 第二个目标：username=xiaowang&password=12345&age=18&sex=女&score=90

    var newStr = arr.join("&");
    console.log(newStr);

    var newUrl = url + "?" + newStr;
    console.log(newUrl);
</script>
</body>
</html>
```

## 十九、图片轮播
### 01.图片轮播布局
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>07.图片轮播布局</title>
    <link rel="stylesheet" href="reset.css">
    <style>
        #outer{
            width: 700px;
            border: 1px solid #000;
            margin: 40px auto;
            position: relative;
        }
        #inner{
            overflow: scroll;
        }
        #con{
            width: 4000px;
            overflow: hidden;
        }
        #con img{
            float: left;
            width: 700px;
            height: 400px;
        }

        #left{
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background-color: rgba(0,0,0,.5);
            font-size: 30px;
            line-height: 50px;
            text-align: center;
            color: #fff;
            position: absolute;
            left: 0;
            top: 50%;
            margin-top: -25px;
        }
        #right{
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background-color: rgba(0,0,0,.5);
            font-size: 30px;
            line-height: 50px;
            text-align: center;
            color: #fff;
            position: absolute;
            right: 0;
            top: 50%;
            margin-top: -25px;
        }

        #list{
            overflow: hidden;
            position: absolute;
            bottom: 10px;
            left: 50%;
            margin-left: -100px;
        }
        #list li{
            width: 20px;
            height: 20px;
            background-color: #4c71ff;
            color: #fff;
            text-align: center;
            line-height: 20px;
            margin: 0 10px;
            float: left;

        }
    </style>
</head>
<body>
    <div id="outer">
        <div id="inner">
            <div id="con">
                <img src="../images/01.jpg" alt="">
                <img src="../images/02.jpg" alt="">
                <img src="../images/03.jpg" alt="">
                <img src="../images/04.jpg" alt="">
                <img src="../images/05.jpg" alt="">
            </div>
            <p id="left">&lt;</p>
            <p id="right">&gt;</p>
            <ul id="list">
                <li>1</li>
                <li>2</li>
                <li>3</li>
                <li>4</li>
                <li>5</li>
            </ul>
        </div>
    </div>
    <script>
    </script>
</body>
</html>
```
### 02.图片轮播自动走基础版本
```js
        var oInner = document.getElementById("inner");
        var oCon = document.getElementById("con");
        var oImgs = oCon.getElementsByTagName("img");
        var timer1 = null;//每隔两秒换张图的 计时器
        var v = 0;//定义一个变量 代表当前显示的图片下标

        // timer1 只是控制每隔两秒换一张图
        timer1 = setInterval(function () {
            v ++;
            if (v >= oImgs.length) {
                v = 0;
            }
            oInner.scrollLeft = v * oImgs[0].offsetWidth;
        },2000)
```

### 03.图片轮播自动走
```js
        var oInner = document.getElementById("inner");
        var oLeft = document.getElementById("left");
        var oRight= document.getElementById("right");
        var oCon = document.getElementById("con");
        var oImgs = oCon.getElementsByTagName("img");
        var timer1 = null;//每隔两秒换张图的 计时器
        var timer2 = null;//每次换图的时候，计时器动画
        var v = 0;//定义一个变量 代表当前显示的图片下标

        // timer1 只是控制每隔两秒换一张图
        timer1 = setInterval(function () {
            /*为了防止页面失去焦点后，里边的计时器等待或者紊乱进行叠加
            所以每次开始新的动画时，把上一次的计时器清除掉*/
            clearInterval(timer2);
            v ++;
            if (v >= oImgs.length) {
                v = 0;
            }
            // oInner.scrollLeft = v * oImgs[0].offsetWidth;//这个是最后的结束位置  我们以动画形式呈现

            //起始位置：当前所在位置
            var start = oInner.scrollLeft;
            //结束位置：v * oImgs[0].offsetWidth
            var end = v * oImgs[0].offsetWidth;
            //起始步数： 从0开始  方便计算当起始等于结束 动画结束
            var startStep = 0;
            //结束步数：我们自己定义  步数越多 走的越慢
            var endStep = 55;
            //每一步所走的距离
            var everyStep = (end - start)/(endStep - startStep);

            //每次换图动画
            timer2 = setInterval(function () {
                // 让起始步数加一，然后用来判断动画是否结束
                startStep ++;
                if (startStep >= endStep){
                    clearInterval(timer2);
                }
                //如果说scrollLeft直接参加计算，那么会忽略小数点，所以我们尽量避免scrollLeft直接参加计算
                //而是让变量计算 然后赋值给scrollLeft
                /*console.log(oInner.scrollLeft,everyStep)
                oInner.scrollLeft +=  everyStep;*/

                start += everyStep;
                oInner.scrollLeft = start;
            },10)
        },2000) 
```


### 04.图片轮播点击走
```js
        var oInner = document.getElementById("inner");
        var oLeft = document.getElementById("left");
        var oRight= document.getElementById("right");
        var oCon = document.getElementById("con");
        var oList = document.getElementById("list");
        var oImgs = oCon.getElementsByTagName("img");
        var oLis = oList.getElementsByTagName("li");
        var timer1 = null;//每隔两秒换张图的 计时器
        var timer2 = null;//每次换图的时候，计时器动画
        var v = 0;//定义一个变量 代表当前显示的图片下标

        // 图片切换动画代码
        function move(){

            // oInner.scrollLeft = v * oImgs[0].offsetWidth;//这个是最后的结束位置  我们以动画形式呈现
            //起始位置：当前所在位置
            var start = oInner.scrollLeft;
            //结束位置：v * oImgs[0].offsetWidth
            var end = v * oImgs[0].offsetWidth;
            //起始步数： 从0开始  方便计算当起始等于结束 动画结束
            var startStep = 0;
            //结束步数：我们自己定义  步数越多 走的越慢
            var endStep = 55;
            //每一步所走的距离
            var everyStep = (end - start)/(endStep - startStep);

            //每次换图动画
            timer2 = setInterval(function () {
                // 让起始步数加一，然后用来判断动画是否结束
                startStep ++;
                if (startStep >= endStep){
                    clearInterval(timer2);
                }
                //如果说scrollLeft直接参加计算，那么会忽略小数点，所以我们尽量避免scrollLeft直接参加计算
                //而是让变量计算 然后赋值给scrollLeft
                /*console.log(oInner.scrollLeft,everyStep)
                oInner.scrollLeft +=  everyStep;*/

                start += everyStep;
                oInner.scrollLeft = start;
            },10)
        }
        //页码切换函数
        function pageChange(){
            //让小标跟着动
            for (var i = 0; i < oLis.length; i++) {
                if (i == v){
                    oLis[i].className = "show";
                } else {
                    oLis[i].className = "";
                }
            }
        }
        //自动走函数
        function autoMove(){
            // timer1 只是控制每隔两秒换一张图
            timer1 = setInterval(function () {
                /*为了防止页面失去焦点后，里边的计时器等待或者紊乱进行叠加
                所以每次开始新的动画时，把上一次的计时器清除掉*/
                clearInterval(timer2);
                v ++;
                if (v >= oImgs.length) {
                    v = 0;
                }
                move();
                pageChange()
            },2000)
        }

        // 1、刚进入页面调用自动走函数
        autoMove();


        //2、点击右边按钮
        oRight.onclick = function () {
            clearInterval(timer1);
            clearInterval(timer2);
            v ++;
            if (v >= oImgs.length){
                v = 0;
            }
            move();
            pageChange();
            autoMove();
        }

        //3、点击左边按钮
        oLeft.onclick = function () {
            clearInterval(timer1);
            clearInterval(timer2);
            v --;
            if(v < 0){
                v = 4;
            }
            move();
            pageChange();
            autoMove();
        }


        ///4、给下标绑定点击事件
        for (var i = 0; i < oLis.length; i++) {
            oLis[i].onclick = function () {
                clearInterval(timer1);
                clearInterval(timer2);
                for (var j = 0; j < oLis.length; j++) {
                    if (oLis[j] == this){
                        oLis[j].className = "show";
                        // j代表当前点击的下标，当点击按钮以后，让v等于当前下标  v代表要走到的图片
                        v = j;
                        move();
                        autoMove();
                    } else{
                        oLis[j].className = "";
                    }
                }
            }
        }
```

### 05.图片轮播无缝版
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>11.封装</title>
    <link rel="stylesheet" href="reset.css">
    <style>
        #outer{
            width: 700px;
            border: 1px solid #000;
            margin: 40px auto;
            position: relative;
        }
        #inner{
            overflow: scroll;
        }
        #con{
            width: 4500px;
            overflow: hidden;
        }
        #con img{
            float: left;
            width: 700px;
            height: 400px;
        }

        #left{
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background-color: rgba(0,0,0,.5);
            font-size: 30px;
            line-height: 50px;
            text-align: center;
            color: #fff;
            position: absolute;
            left: 0;
            top: 50%;
            margin-top: -25px;
        }
        #right{
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background-color: rgba(0,0,0,.5);
            font-size: 30px;
            line-height: 50px;
            text-align: center;
            color: #fff;
            position: absolute;
            right: 0;
            top: 50%;
            margin-top: -25px;
        }

        #list{
            overflow: hidden;
            position: absolute;
            bottom: 10px;
            left: 50%;
            margin-left: -100px;
        }
        #list li{
            width: 20px;
            height: 20px;
            background-color: #4c71ff;
            color: #fff;
            text-align: center;
            line-height: 20px;
            margin: 0 10px;
            float: left;
        }
        #list .show{
            background-color: mediumvioletred;
        }
    </style>
</head>
<body>
    <div id="outer">
        <div id="inner">
            <div id="con">
                <img src="../images/01.jpg" alt="">
                <img src="../images/02.jpg" alt="">
                <img src="../images/03.jpg" alt="">
                <img src="../images/04.jpg" alt="">
                <img src="../images/05.jpg" alt="">
                <img src="../images/01.jpg" alt="">
            </div>
            <p id="left">&lt;</p>
            <p id="right">&gt;</p>
            <ul id="list">
                <li class="show">1</li>
                <li>2</li>
                <li>3</li>
                <li>4</li>
                <li>5</li>
            </ul>
        </div>
    </div>
    <script>
        var oInner = document.getElementById("inner");
        var oLeft = document.getElementById("left");
        var oRight= document.getElementById("right");
        var oCon = document.getElementById("con");
        var oList = document.getElementById("list");
        var oImgs = oCon.getElementsByTagName("img");
        var oLis = oList.getElementsByTagName("li");
        var timer1 = null;//每隔两秒换张图的 计时器
        var timer2 = null;//每次换图的时候，计时器动画
        var v = 0;//定义一个变量 代表当前显示的图片下标
        // var page = 0;
        // 图片切换动画代码
        function move(){

            // oInner.scrollLeft = v * oImgs[0].offsetWidth;//这个是最后的结束位置  我们以动画形式呈现
            //起始位置：当前所在位置
            var start = oInner.scrollLeft;
            //结束位置：v * oImgs[0].offsetWidth
            var end = v * oImgs[0].offsetWidth;
            //起始步数： 从0开始  方便计算当起始等于结束 动画结束
            var startStep = 0;
            //结束步数：我们自己定义  步数越多 走的越慢
            var endStep = 55;
            //每一步所走的距离
            var everyStep = (end - start)/(endStep - startStep);

            //每次换图动画
            timer2 = setInterval(function () {
                // 让起始步数加一，然后用来判断动画是否结束
                startStep ++;
                if (startStep >= endStep){
                    clearInterval(timer2);
                }
                //如果说scrollLeft直接参加计算，那么会忽略小数点，所以我们尽量避免scrollLeft直接参加计算
                //而是让变量计算 然后赋值给scrollLeft
                /*console.log(oInner.scrollLeft,everyStep)
                oInner.scrollLeft +=  everyStep;*/

                start += everyStep;
                oInner.scrollLeft = start;
            },10)
        }
        //页码切换函数
        function pageChange(){
            //让小标跟着动
            //因为v可以是5  但是i最大是4
            /*但是 v为5的时候 其实代表的是第一张图 也就是 i = 0
            但是我们不能随意修改v  因为v代表的是图片  只有图片滚动的时候才能改变v
            所以定义一个变量page 保存v  和i相关
            判断当page 等于5的时候  让page = 0*/
            var page = v;
            for (var i = 0; i < oLis.length; i++) {
                if (page == 5){
                    page = 0;
                }
                if (i == page){
                    oLis[i].className = "show";
                } else {
                    oLis[i].className = "";
                }
            }
        }
        //自动走函数
        function autoMove(){
            // timer1 只是控制每隔两秒换一张图
            timer1 = setInterval(function () {
                /*为了防止页面失去焦点后，里边的计时器等待或者紊乱进行叠加
                所以每次开始新的动画时，把上一次的计时器清除掉*/
                clearInterval(timer2);
                v ++;
                //当 v走到第六张（新添加的1）  再加的时候 应该走第二个图  所以v应该等于1
                //当最后一张 图1 要走图二的时候  应该瞬间让滚动条变成最前的图1  也就是滚动条为0
                if (v >= oImgs.length) {
                    oInner.scrollLeft = 0;
                    v = 1;
                }
                move();
                pageChange()
            },2000)
        }

        // 1、刚进入页面调用自动走函数
        autoMove();


        //2、点击右边按钮
        oRight.onclick = function () {
            clearInterval(timer1);
            clearInterval(timer2);
            v ++;
            if (v >= oImgs.length) {
                oInner.scrollLeft = 0;
                v = 1;
            }
            move();
            pageChange();
            autoMove();
        }

        //3、点击左边按钮
        oLeft.onclick = function () {
            clearInterval(timer1);
            clearInterval(timer2);
            v --;
            if(v < 0){
                v = oImgs.length - 2;
                oInner.scrollLeft = (oImgs.length - 1) * oImgs[i].offsetWidth;
            }
            move();
            pageChange();
            autoMove();
        }


        ///4、给下标绑定点击事件
        for (var i = 0; i < oLis.length; i++) {
            oLis[i].onclick = function () {
                clearInterval(timer1);
                clearInterval(timer2);
                for (var j = 0; j < oLis.length; j++) {
                    if (oLis[j] == this){
                        oLis[j].className = "show";
                        // j代表当前点击的下标，当点击按钮以后，让v等于当前下标  v代表要走到的图片
                        v = j;
                        move();
                        autoMove();
                    } else{
                        oLis[j].className = "";
                    }
                }
            }
        }
    </script>
</body>
</html>
```


## 二十、常见window事件
### 01.onload事件
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>onload</title>
    <script>
        
    </script>
</head>
<body>
    <img src="../images/07.jpg" alt="" id="img">
<script>
    var oImg = document.getElementById("img");
    /*当图片没有设置宽高的时候，想到得到图片的宽高，需要等待图片加载进来以后才能获取到，
    否则获取不到  直接获取的就是0
    当图片设置宽高，那么我们随时获取的图片宽度 都是DOM节点你设置的宽度，而不是图片真正的宽度*/


    console.log(oImg.offsetWidth);//0

    // 把获取图片的宽度放在计时器中
    setTimeout(function () {
        // 因为图片加载的会慢，但是在DOM节点读取完以后，在执行js的时，图片可能还在加载，所以获取的图片为0
        // 给一个延迟执行，那么可能图片就会加载完毕，然后打印出图片的宽度
        console.log(oImg.offsetWidth + "计时器的");//1920
    },1000)


    // 书写计时器等待图片加载时间不好控制，所以onload事件是等待资源加载完毕以后执行
    oImg.onload = function () {
        console.log(oImg.offsetWidth + "onload");//1920
    }
</script>
</body>
</html>
```
### 02.进度条
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>进度条</title>
    <style>
        .progress{
            width: 400px;
            height: 50px;
            border: 2px solid #009ff2;
        }
        .box{
            width: 0%;
            height: 50px;
            background-color: orangered;
        }
    </style>
</head>
<body>
<div class="progress">
    <div class="box"></div>
</div>
<div id="con">已经加载了 0%</div>
<script>
    var oCon = document.getElementById("con");
    var oProgress = document.querySelector(".progress");
    var oBox = document.querySelector(".box");
    var num = 0;
    for (var i = 0; i < 30; i++) {
        var v = i + 1;
        var newImg = new Image();
        v < 10 ? v = "0" + v : v;
        newImg.src = "../images/" + v + ".jpg";

        newImg.onload = function () {
            num ++;
            oBox.style.width = num / 30 * 100 + "%";
            oCon.innerHTML = `已经加载了 ${parseInt(num / 30 * 100)}%`
        }
    }
</script>
</body>
</html>
```
### 03.window.onload
- window.onload事件在页面完全加载完毕的时候触发。该事件包含所有的图形图像，外部文件的加载，也就是说在页面所有的内容全部加载之前，任何DOM操作都不会发生
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>window.onload</title>
    <script>
        // js是可以放在这个位置的，
        // 但是在这个位置的js 直接获取元素是会获取不到的  因为代码还没有运行到DOM节点
       /* var oBox = document.getElementById("box");
        oBox.style.backgroundColor = "red";*/

       // 解决方法：添加window.onload
        window.onload = function () {
            var oBox = document.getElementById("box");
            oBox.style.backgroundColor = "red";
        }

    </script>

</head>
<body>
<div id="box">我是box</div>
<img src="../images/01.jpg" alt="">
<img src="../images/02.jpg" alt="">
<img src="../images/03.jpg" alt="">
<img src="../images/04.jpg" alt="">
<script>
// window.onload事件：当整个文档内容（DOM节点+所需要的资源（音频、视频、图片、程序等等））全部加载完毕，才会执行
/*window.onload = function () {
    var oImgs = document.getElementsByTagName("img");
    for (var i = 0; i < oImgs.length; i++) {
        console.log(oImgs[i].offsetWidth);
    }
}*/
</script>
</body>
</html>
```

### 03.window.unload
- 页面卸载，这个事件在超链接、前进、yy h后退或者关闭窗口时触发。
- beforeunload 类型和unload功能类似，不过更人性化，如果beforeunload事件处理函数返回字符串，则该字符串会显示在一个确认的对话框中，询问是否离开。
```js
    localStorage.setItem("hello","world");
    /*window.onunload = function () {
        localStorage.removeItem("hello");
    }*/

    window.onbeforeunload = function () {
        localStorage.removeItem("hello");
        return "你确定你要走？？？"
    }
```
### 03.onscroll事件
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>onscroll</title>
    <style>
        #outer{
            width: 400px;
            height: 300px;
            border:1px solid #000;
            overflow: scroll;
        }
        #con{
            width: 800px;
            height: 1000px;
        }
    </style>
    <script>
        window.onload = function () {
            // onscroll是滚动条滚动即执行
            var oOuter = document.getElementById("outer");
            var oCon = document.getElementById("con");
            oOuter.onscroll = function () {
                console.log(Date.now());//只要在滚动  那么每次间隔最小可能是十几毫秒 甚至2毫秒  所以onscroll事件执行特别的频繁
                console.log("我滚了 再见");
            }
        }
    </script>
</head>
<body>
<div id="outer">
    <div id="con">
        今天天气真好 <br>
        今天天气真好 <br>
        今天天气真好 <br>
        今天天气真好 <br>
        今天天气真好 <br>
        今天天气真好 <br>
        今天天气真好 <br>
        今天天气真好 <br>
        今天天气真好 <br>
        今天天气真好 <br>
        今天天气真好 <br>
        今天天气真好 <br>
        今天天气真好 <br>
        今天天气真好 <br>
        今天天气真好 <br>
    </div>
</div>
</body>
</html>
```

### 04.window.onscroll
- scroll事件类型是用于在浏览器内移动文档的位置时触发。
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>window.onscroll</title>
    <style>
        body{
            height: 3000px;
            background-color: pink;
        }
    </style>
</head>
<body>
<script>
    // window.onscroll：当系统滚动条滚动的时候触发
    window.onscroll = function () {
        console.log("滚了吧");
    }
</script>
</body>
</html>
```

### 05.resize事件
- 窗口重置，resize事件是在浏览器窗口被重置时触发。
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>window.onresize</title>
    <script src="./my.js"></script>
</head>
<body>
<script>，
    // 目前 只有浏览器窗口大小改变才能出发onresize事件
    function changeColor() {
        if (my.getScreen().width >= 1000){
            document.body.style.backgroundColor = "red";
        }else if (my.getScreen().width >= 800){
            document.body.style.backgroundColor = "yellow";
        }else if(my.getScreen().width >= 600){
            document.body.style.backgroundColor = "green";
        }else{
            document.body.style.backgroundColor = "blue";
        }
    }
    /*// 方法1：页面调用的时候先执行一次
    changeColor();
    window.onresize = changeColor;*/

    // 方法二 合写

   /* window.onload = changeColor;
    window.onresize = changeColor;*/

    window.onload = window.onresize = changeColor;
</script>
</body>
</html>
```

### 06.节流函数
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>节流函数</title>
    <script src="my.js"></script>
    <style>
        body{
            height: 5000px;
        }
    </style>
</head>
<body>
<script>
    // 节流就是优化高频率执行js代码的一种手段。
    // oninput,onkeypress,onscroll,resize等事件触发频率非常高，那么如果在这些事件触发时执行代码，就会相应的将代码块执行很多次。
    // 但是通常大量的重复执行是没有必要的节流就是保证一段时间内只执行一次核心代码
    var i = 0;
    // 定义一个节流函数的开关  默认开启
    var flag = true;
    function fn1(){
        i++;
        console.log("滚了"+ i);
    }
    window.onscroll = function(){
        //当开关是关闭的状态 那么就不执行函数
        if(!flag){
           return;
        }

        // 当flag开启了 进入功能函数执行了，我们要先把开关给关闭了
        flag = !flag;
        //调用函数
        fn1();
        /*当函数执行完成以后，延迟200毫秒 再把开关打开，下一次的事件才能进来
        这样可以节省很多次函数的运行  并且用户体验也不会变差*/
        setTimeout(function () {
            flag = ! flag;
        },200)

    }
</script>
</body>
</html>
```

### 07.图片轮播节流版本
```js
    window.onload = function () {
        var oInner = document.querySelector(".inner");
        var oImgs = document.querySelectorAll(".con>img");
        var oLeft = document.querySelector(".left");
        var oRight = document.querySelector(".right");
        var oLis = document.querySelectorAll(".page>li");
        var timer1 = null;
        var timer2 = null;
        var i = 0;//代表图片  默认第一张
        var flag = true;

        // 图片更换动画函数z
        function move(){
            //在每一个两秒内，不让滚动条直接走，而是以动画形式移动
            var start = oInner.scrollLeft;//当前滚动条的位置
            var end = i * oImgs[0].offsetWidth;//每次动画的结束位置
            var startStep = 0;
            var endStep = 44;
            var everyStep = (end - start) / (endStep - startStep);//每一步所走的距离

            //让滚动条条动画移动
            timer2 = setInterval(function () {
                startStep ++;//用来判断动画是否执行完毕
                if (startStep >= endStep) {
                    clearInterval(timer2);
                    flag = !flag;
                }

                // oInner.scrollLeft += everyStep;//scroll直接参与运算是向下取整的，start是默认当前滚动条位置，所以让变量start运算即可

                start += everyStep;
                oInner.scrollLeft = start;
            },20)
        }

        //自动走函数
        function autoMove(){
            //每隔两秒就换图
            timer1 = setInterval(function () {
                // 在每一次新的一个动画开始的时候，先把上一次的动画给清掉
                clearInterval(timer2);
                i ++;
                if (i >= oImgs.length){
                    i = 0;
                }
                move();
                page();
            },2000)
        };

        //清计时器
        function clear(){
            clearInterval(timer1);
            clearInterval(timer2);
        }

        //下标跟着走函数
        function page() {
            // 让下标跟着图片
            for (var j = 0; j < oLis.length; j++) {
                if( i == j ){
                    oLis[j].classList.add("show");
                }else{
                    oLis[j].classList.remove("show");
                }
            }
        }

        //页面加载后 自动走
        autoMove();

        //点击左边按钮
        oLeft.onclick = function () {
            if (!flag) {
                return;
            }
            flag = !flag;
            //先把所有计时器给清掉
            clear();
            i ++;
            if (i >= oImgs.length){
                i = 0;
            }
            move();
            page();
            //每次点击事件执行完成后，执行自动走
            autoMove();
        }

        //点击右边按钮
        oRight.onclick = function(){
            if (!flag) {
                return;
            }
            flag = !flag;
            clear();
            i --;
            if (i < 0){
                i = oImgs.length - 1;
            }
            move();
            page();
            autoMove();
        }


        //给下标绑定点击事件
        for (var j = 0; j < oLis.length; j++) {
            oLis[j].onclick = function () {
                clear();
                for (var k = 0; k < oLis.length; k++) {
                    if (oLis[k] == this){
                        oLis[k].classList.add("show");

                        //i是图片轮播的核心，所以让i和当前点击的下标相等
                        i = k
                        move();
                    }else{
                        oLis[k].classList.remove("show");
                    }
                }
            }
        }
    }
```

### 08.延迟加载（懒加载）
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>延迟加载（懒加载）</title>
    <link rel="stylesheet" href="./reset.css">
    <style>
        .box{
            width: 1040px;
            margin: 0 auto;
            overflow: hidden;
        }
        .box img{
            width: 500px;
            height: 300px;
            margin: 10px;
            float: left;
        }
    </style>
</head>
<body>
<div id="box" class="box">
    <img src="../images/loading.gif" orc="../images/01.jpg" alt="">
    <img src="../images/loading.gif" orc="../images/02.jpg" alt="">
    <img src="../images/loading.gif" orc="../images/03.jpg" alt="">
    <img src="../images/loading.gif" orc="../images/04.jpg" alt="">
    <img src="../images/loading.gif" orc="../images/05.jpg" alt="">
    <img src="../images/loading.gif" orc="../images/06.jpg" alt="">
    <img src="../images/loading.gif" orc="../images/07.jpg" alt="">
    <img src="../images/loading.gif" orc="../images/08.jpg" alt="">
    <img src="../images/loading.gif" orc="../images/09.jpg" alt="">
    <img src="../images/loading.gif" orc="../images/10.jpg" alt="">
    <img src="../images/loading.gif" orc="../images/11.jpg" alt="">
    <img src="../images/loading.gif" orc="../images/12.jpg" alt="">
    <img src="../images/loading.gif" orc="../images/13.jpg" alt="">
    <img src="../images/loading.gif" orc="../images/14.jpg" alt="">
    <img src="../images/loading.gif" orc="../images/15.jpg" alt="">
    <img src="../images/loading.gif" orc="../images/16.jpg" alt="">
    <img src="../images/loading.gif" orc="../images/17.jpg" alt="">
    <img src="../images/loading.gif" orc="../images/18.jpg" alt="">
    <img src="../images/loading.gif" orc="../images/19.jpg" alt="">
    <img src="../images/loading.gif" orc="../images/20.jpg" alt="">
    <img src="../images/loading.gif" orc="../images/21.jpg" alt="">
    <img src="../images/loading.gif" orc="../images/22.jpg" alt="">
    <img src="../images/loading.gif" orc="../images/23.jpg" alt="">
    <img src="../images/loading.gif" orc="../images/24.jpg" alt="">
    <img src="../images/loading.gif" orc="../images/25.jpg" alt="">
    <img src="../images/loading.gif" orc="../images/26.jpg" alt="">
    <img src="../images/loading.gif" orc="../images/27.jpg" alt="">
    <img src="../images/loading.gif" orc="../images/28.jpg" alt="">
    <img src="../images/loading.gif" orc="../images/29.jpg" alt="">
    <img src="../images/loading.gif" orc="../images/30.jpg" alt="">
    <img src="../images/loading.gif" orc="../images/31.jpg" alt="">
    <img src="../images/loading.gif" orc="../images/32.jpg" alt="">

</div>
<script src="./my.js"></script>
<script>
    // 页面加载图片等资源的时候，要花费大量的时间和带宽，如果说进行懒加载 则节省流量

    var oBox = my.getID("box");
    var oImgs = oBox.getElementsByTagName("img");
    var flag = true;
    // 定义一个变量，保存已经加载过的图片数量 默认为0
    var n = 0;
    //当页面滚动滚动条的时候，开启节流函数
    window.onscroll = function(){
        //当开关是关闭的状态 那么就不执行函数
        if(!flag){
            return;
        }

        // 当flag开启了 进入功能函数执行了，我们要先把开关给关闭了
        flag = !flag;
        //调用函数
        lazyLoad();
        /*当函数执行完成以后，延迟200毫秒 再把开关打开，下一次的事件才能进来
        这样可以节省很多次函数的运行  并且用户体验也不会变差*/
        setTimeout(function () {
            flag = ! flag;
        },200)

    }
    //当页面刚进入的时候  先调用一次判断函数 看是否加载图片
    lazyLoad();
    function lazyLoad() {
        //1.获取系统滚动条滚过去的距离
        // my.getWinScroll().top
        //2.获取屏幕窗口的高度
        //my.getScreen().height

        /*3、只要函数被调用，那么就遍历所有的img
        当img距离文档顶部长度 小于等于  滚动条滚过去的距离+窗口的高度   那么就进行加载图片*/

        for (var i = n; i < oImgs.length; i++) {
            if (my.getEleToDoc(oImgs[i]).top <= my.getWinScroll().top + my.getScreen().height) {
                oImgs[i].src = oImgs[i].getAttribute("orc");
                // 每次有图片加载 就让n+1
                // 每次刚开始for循环的时候  就让i赋值为n 可以跳过已经加载过的图片  增加效率
                n ++;
            }
        }
    }
</script>
</body>
</html>
```

## 二十一、事件处理
### 01.事件模型
- 基本事件模型:也称为DOM0事件模型,是浏览器初期出现的一种比较简单的事件模型,主要通过HTML事件属性,为指定标签绑定事件处理函数。由于这种模型应用比较广泛,获得了所有浏览器的支持,目前依然比较流行。但是这种模型对于HTML文档标签依赖严重,不利于JavaScript独立开发

- DOM事件模型:由W3C制订,是目前标准的事件处理模型。所有符合标准的浏览器都支持该模型,IE怪异模式不支持。DOM事件模型包括DOM2事件模块和DOM3事件模块,DOM3事件模块为DOM2事件模块的升级版,略有完善,主要是新增了一些事情类型,以适应移动设备的开发需要,但大部分规范和用法保持一致。

- IE事件模型:IE4.0及其以上版本浏览器支持,与DOM事件模型相似,但用法不同

- Netscape事件模型:由 Netscape4浏览器实现,在 Netscape6中停止支持

### 02.事件流
事件流就是多个节点对象对同一种事件进行响应的先后顺序,主要包括以下3种类型
- 冒泡型 事件从最特定的目标向最不特定的目标( document对象)触发,也就是事件从下向上进行响应,这 个传递过程被形象地称为“冒泡”

- 捕获型 事件从最不确定的目标（document对象）开始触发，然后到最特定的目标，也就是事件从上向下进行相应

- 混合型 w3C的DOM事件模型支持捕获型和冒泡型两种事件流,其中捕获型事件流先发生,然后才发生冒泡型事件流。两种事件流会触及DOM中的所有层级对象,从 document对象开始,最后返回 document对象结束。因此,可以把事件传播的整个过程分为3个阶段 **捕获阶段**:事件从 document对象沿着文档树向下传播到目标节点,如果目标节点的任何一个上级节点注册了相同的事件,那么事件在传播的过程中就会首先在最接近顶部的上级节点执行,依
次向下传播 **目标阶段**:注册在目标节点上的事件被执行 **冒泡阶段**:事件从目标节点向上触发,如果上级节点注册了相同的事件,将会逐级响应,依次向上传播

### 03.绑定事件
- 静态绑定：把JS脚本作为属性值，直接负值给事件属性
- 动态绑定：使用DOM对象的事件属性进行赋值
- 事件处理函数：事件处理函数是一类特殊的函数，与函数直接量结构相同，主要任务是实现事件处理，为异步调用，由事件触发进行相应。
### 04.绑定事件的事件机制（DOM0事件）
```js
    // 使用on+事件名这种方式注册的事件叫做DOM0级事件 所有浏览器都支持这种事件绑定

    var oOuter = my.getID("outer");
    var oInner = my.getID("inner");
    var oCon = my.getID("con");

    //DOM 0级事件 在所有浏览器中都是冒泡的形式
    oOuter.onclick = function () {
        alert("outer");
    }
    oInner.onclick = function () {
        alert("inner");
    }
    oCon.onclick = function () {
        alert("con");
    }
```

```js
    var oBox = document.getElementById("box");
        /*使用DOM0级事件 对同一个元素绑定同一个事件 只能执行一次
        后边的绑定会把前边的绑定给覆盖掉*/
        /*oBox.onclick = function () {
            alert(1);
        }
        oBox.onclick = function () {
            alert(2);
        }
        oBox.onclick = function () {
            alert(3);
        }
        oBox.onclick = function () {
            alert(4);
        }*/


        oBox.onclick = function () {
            alert(4);
        }
        // 取消DOM 0 级事件  直接给事件一个null即可
        document.onclick = function () {
            oBox.onclick = null;
        }
```

### 05.注册事件
- 在DOM事件模型中，通过调用对象的addEventListnenr()方法注册事件
- type:注册事件的类型名,事件类型与事件属性不同,事件类型名没有on前缀,例如,对于事件属性 onclick来说,所对应的事件类型为 click
- listener:监听函数,即事件处理函数,在指定类型的事件发生时将调用该函数,在调用这个函数时,默认传递给它的唯一参数是 event对象
- useCapture:是一个布尔值,如果为true,则指定的事件处理函数将在事件传播的捕获阶段触发，如果为 false,则事件处理函数将在冒泡阶段触发
- 使用 addEventListener()方法能够为多个对象注册相同的事件处理函数,也可以为同一个对象注册多件处理函数。为同一个对象注册多个事件处理函数对于模块化开发非常有用。
- IE事件模型使用attachEvent(etype,eventName)
    etype:事件类型：onclick、onkeyup等
    eventName：设置事件处理函数
    使用attachEvent注册事件时，其事件处理函数的调用对象不再是当前事件对象的本身，而是window对象，如果想要获取当前对象，则使用event事件对象
``` html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>注册事件（事件监听）</title>
</head>
<body>
    <div id="demo">demo</div>
    <div id="outer">
        <div id="inner">
            <div id="con">
                k看我的事件流
            </div>
        </div>
    </div>
<script>

    var oDemo = document.getElementById("demo");
    /*oDemo.addEventListener("click",function () {
        alert("demo1");
    },false);
    oDemo.addEventListener("click",function () {
        alert("demo2");
    },false);
    oDemo.addEventListener("click",function () {
        alert("demo3");
    },false);
    oDemo.addEventListener("click",function () {
        alert("demo4");
    },false);*/



    var oOuter = document.getElementById("outer");
    var oInner = document.getElementById("inner");
    var oCon = document.getElementById("con");
    /*oOuter.addEventListener("click",function () {
        alert("outer")
    },false)
    oInner.addEventListener("click",function () {
        alert("inner")
    },true)
    oCon.addEventListener("click",function () {
        alert("con")
    },true)*/


    // IE低版本事件监听
    /*oCon.attachEvent("onclick",function () {
        alert(1);
    })
    oInner.attachEvent("onclick",function () {
        alert(2);
    })*/



</script>
</body>
</html>
```

### 06.销毁事件
- 在DOM事件模型中，使用removeEventListener()方法可以从指定对象中删除已经注册的事件处理函数
- removeEventListener()只能处理addEventListener方法注册的事件
- 当临时注册一个事件时，可以在处理完毕后删掉它，这样嫩个够节省系统资源
- IE事件模型使用detachEvent方法注销事件
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
<div id="box">点击我有惊喜哦</div>
<button id="btn">取消惊喜</button>
<script>
    var oBox = document.getElementById("box");
    var oBtn = document.getElementById("btn");

    /*oBox.onclick = function () {
        alert("圣诞快乐");
    }
    //点击btn 取消box的DOM0点击事件
    oBtn.onclick = function () {
        oBox.onclick = null;
    }*/


    // 必须保证绑定的函数和移除的函数是同一个函数
    /*function f(){
        alert("圣诞快乐")
    }
    oBox.addEventListener("click",f,false);
    //点击btn 取消box的DOM2点击事件
    oBtn.onclick = function () {
        oBox.removeEventListener("click",f)
    }*/



    function f(){
        alert("圣诞快乐")
    }
    oBox.attachEvent("onclick",f);
    
    oBtn.onclick = function () {
        oBox.detachEvent("onclick",f)
    }
</script>
</body>
</html>
```

### 07.绑定事件兼容
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>DOM2级事件的兼容</title>
</head>
<body>
<button id="btn">移除事件</button>
<div id="box">
box
</div>
<script src="./my.js"></script>
<script>
    var oBox = document.getElementById("box");
    var oBtn = document.getElementById("btn");
    function fn1() {
        alert("看我");
    }

    /*function addEvent(ele,type,fn,boo) {
        // DOM2级事件绑定兼容性封装
        if (ele.addEventListener){
            ele.addEventListener(type,fn,boo||false);
        }else if (ele.attachEventhEvent){
            ele.attachEvent("on"+type,fn)
        }else{
            ele["on"+type] = fn;
        }
    }*/
    my.addEvent(oBox,"click",fn1)

    /*function removeEvent(ele,type,fn){
        if (ele.removeEventListener){
            ele.removeEventListener(type,fn);
        }else if(ele.detachEvent){
            ele.detachEvent("on"+type,fn)
        }else{
            ele["on" + type] = null;
        }
    }*/

    oBtn.onclick = function () {
        my.removeEvent(oBox,"click",fn1)
    }
    /*// DOM2级事件绑定兼容性封装
    if (oBox.addEventListener){
        oBox.addEventListener("click",fn1,false);
    }else if (oBox.attachEvent){
        oBox.attachEvent("onclick",fn1)
    }else{
        oBox.onclick = fn1;
    }


    oBtn.onclick = function () {
        if (oBox.removeEventListener){
            oBox.removeEventListener("click",fn1);
        }else if(oBox.detachEvent){
            oBox.detachEvent("onclick",fn1)
        }else{
            oBox.onclick = null;
        }
    }*/

</script>
</body>
</html>
```

### 08.DOMContentLoaded事件
- window.onload当所有的节点和资源加载完成才执行
- 加载需要等待资源加载 并且还只能对window绑定一次
- 解决方法1： 仍然是等资源加载完成才执行
- 解决方法2  使用DOMContentLoaded事件  ：当所有节点加载完毕就可以执行
- DOMContentLoaded是DOM2级的事件  需要使用DOM2的监听方式来绑定事件
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>DOMContentLoaded</title>
    <script>
        // window.onload当所有的节点和资源加载完成才执行
        // 加载需要等待资源加载 并且还只能对window绑定一次
        /*window.onload = function () {
            var oBox = document.getElementById("box");
            oBox.onclick = function () {
                alert(1);
            }
        }*/

        //解决方法1： 仍然是等资源加载完成才执行
        /*window.addEventListener("load",function () {
            var oBox = document.getElementById("box");
            oBox.onclick = function () {
                alert(1);
            }
        })*/


        //解决方法2  使用DOMContentLoaded事件  ：当所有节点加载完毕就可以执行
        // onDOMContentLodeaded是DOM2级的事件  需要使用DOM2的监听方式来绑定事件
        window.addEventListener("DOMContentLoaded",function () {
            var oBox = document.getElementById("box");
            oBox.onclick = function () {
                alert(1);
            }
        },false)

    </script>
</head>
<body>
    <div id="box">1111</div>
</body>
</html>
```

### 09.event对象
- event对象由事件自动创建,记录了当前事件的状态,如事件发生的源节点、键盘按键的响应状态、鼠标指针的移动位置、鼠标按键的响应状态等信息, 
- event对象的属性提供了有关事件的细节,其方法可以控制事件的传播
- 2级DOM Events规范定义了一个标准的事件模型,它被除了IE低版本以外的所有现代浏览器所实现,而IE定义了专用的、不兼容的模型。简单比较两种事件模型如下：在DOM事件模型中, event对象被传递给事件处理函数,但是在IE事件模型中,它被存储在window对象的event属性中
>bubbles：返回布尔值,指示事件是否是冒泡事件类型。如果事件是冒泡类型,则返回tue:否则返回 fasle
>cancelable:返回布尔值,指示事件是否可以取消的默认动作,如果使用 preventDefault方法可以取消与事件关联的默认动作则返回值为mue:否则为false
>target:返回事件的目标节点
>type:事件类型
>preventDefault():通知浏览器不要执行与事件关联的默认动作
>stopPropagation():阻止事件在捕获、目标、冒泡阶段的进一步传播
```js
    var oBox = document.getElementById("box");
    /*oBox.onclick = function () {
        console.log(window.event);
        // console.log(1);
    }
    oBox.onclick = function (e) {
        console.log(e);
        // console.log(1);
    }*/

    // 兼容性获取event事件对象：
    oBox.onclick = function (e) {
        var e = e || window.event;
        console.log(e);
    }
```

### 10.event事件的鼠标定位
>clientX:以浏览器窗口左上顶角为原点,定位x轴坐标
>offsetX:以当前事件的目标对象左上顶角为原点,定位x轴坐标
>pageX:以 document对象(即文档窗口)左上顶角为原点,定位x轴坐标(不兼容IE)
>screenX:计算机屏幕左上顶角为原点,定位x轴坐标
```js
    var oCon = document.getElementById("con");
    oCon.onclick = function (e) {
        var e = e || window.event;
        // console.log(e.clientX,e.clientY);
        // console.log(e.offsetX,e.offsetY);
        // console.log(e.pageX,e.pageY);
        // console.log(e.screenX,e.screenY);

        console.log(getEventPage(e));
    }

    // pageX和pageY的封装
    function getEventPage(e) {
        if (e.pageX){
            return {
                x:e.pageX,
                y:e.pageY
            }
        }else{
            return {
                x:document.body.scrollLeft + e.clientX,
                y:document.body.scrollTop + e.clientY
            }
        }
    }
```

### 11.鼠标跟随移动
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>鼠标跟随移动</title>
    <style>
        body{
            height: 3000px;
        }
        img{
            width: 20px;
            height: 20px;
            position: absolute;
            left: 0;
            top: 0;
        }
    </style>
</head>
<body>
<img id="img" src="../images/heart.png" alt="">
<script src="./my.js"></script>
<script>
    var oImg = my.getID("img")
    document.onmousemove = function (ev) {
        var ev = ev || window.event;
        oImg.style.left = ev.clientX + "px";
        oImg.style.top = ev.clientY + "px";
    }
</script>
</body>
</html>
```

### 12.拖影
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>拖影</title>
    <style>
        body{
            height: 3000px;
        }
        img{
            width: 20px;
            height: 20px;
            position: absolute;
            left: 0;
            top: 0;
        }
    </style>
</head>
<body>
<img class="img" src="../images/heart.png" alt="">
<img class="img" src="../images/heart.png" alt="">
<img class="img" src="../images/heart.png" alt="">
<img class="img" src="../images/heart.png" alt="">
<img class="img" src="../images/heart.png" alt="">
<img class="img" src="../images/heart.png" alt="">
<img class="img" src="../images/heart.png" alt="">
<img class="img" src="../images/heart.png" alt="">
<img class="img" src="../images/heart.png" alt="">
<img class="img" src="../images/heart.png" alt="">
<script src="./my.js"></script>
<script>
    var oImgs = document.getElementsByTagName("img");
    // var timer = null;
    document.onmousemove = function (ev) {
        var ev = ev || window.event;
        var  v = -1;//每次移动事件发生  都需要把v清空为-1  就可以重新对所有的img控制
        // 每个计时器都应该有自己的timer 这样当前计时器中清的timer  才是清自己的
        var timer = setInterval(function () {
            v ++;
            if(v >= oImgs.length - 1){
                clearInterval(timer);
            }
            console.log(v);
            oImgs[v].style.left = ev.clientX + "px";
            oImgs[v].style.top = ev.clientY + "px";
        },20)
    }
</script>
</body>
</html>
```

### 13.阻止传播
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>阻止传播</title>
    <style>
        #outer{
            width: 100px;
            height: 100px;
            background-color: red;
        }
        #inner{
            width: 100px;
            height: 50px;
            background-color: yellow;
        }
        #box{
            width: 100px;
            height: 20px;
            background-color: pink;
        }
    </style>
</head>
<body>
<div id="outer">
    <div id="inner">
        <div id="box">box</div>
        inner
    </div>
    outer
</div>
<script>
    var oOuter = document.getElementById("outer");
    var oInner = document.getElementById("inner");
    var oBox = document.getElementById("box");


    oOuter.addEventListener("click",function (ev) {
        // ev.stopPropagation?ev.stopPropagation():ev.cancelBubble = true;
        alert(1);
    },true);
    oInner.addEventListener("click",function () {
        alert(2);
    },true);
    oBox.addEventListener("click",function (ev) {
        // 阻止传播
        // 现代浏览器中：
       /* ev.stopPropagation();

        // ie678浏览器中
        ev.cancelBubble = true;*/

        // ev.stopPropagation?ev.stopPropagation():ev.cancelBubble = true;
        alert(3);
    },true);

</script>
</body>
</html>
```

### 14.阻止默认事件
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>阻止默认事件</title>
</head>
<body>
<a id="a1" href="http://www.baidu.com">百度一下你就知道</a>
<script>
    var oA1 = document.getElementById("a1");
    oA1.onclick = function (ev) {
        var ev = ev || window.event;

        // 阻止默认事件
        /*在现代浏览器：
        ev.preventDefault();
        在IE678：
        ev.returnValue = false;*/

        /*if(ev.preventDefault){
            ev.preventDefault();
        }else{
            ev.returnValue = false;
        }*/

        // ev.preventDefault?ev.preventDefault():ev.returnValue = false;

        return false;//如果说用来阻止默认事件，必须写在函数的最下边  因为他下边的代码不再执行
    }
</script>
</body>
</html>
```

### 13.拖拽
#### 01.拖拽方法1
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>拖拽方法一</title>
    <link rel="stylesheet" href="./reset.css">
    <style>
        #box{
            width: 100px;
            height: 100px;
            background-color: red;
            position: absolute;
            left: 0;
            top: 0;
        }
    </style>
</head>
<body>
<div id="box">

</div>
<script src="./my.js"></script>
<script>
    var oBox = my.getID("box");
    // 对obox绑定鼠标按下事件
    oBox.onmousedown = function (ev) {
        var ev = ev ||window.event;
        // 获取鼠标距离当前元素边缘的距离 ，这个距离是一直不会发生改变的
        var mouseDown = {
            left:ev.clientX - my.getEleToDoc(oBox).left,
            top:ev.clientY - my.getEleToDoc(oBox).top
        }
        console.log(mouseDown)
        document.onmousemove = function(ev){
            var ev = ev || window.event;
            //最终鼠标的位置用对象来保存
            var boxPoint = {
                left:ev.clientX - mouseDown.left,
                top:ev.clientY - mouseDown.top
            }
            //赋值
            oBox.style.left = boxPoint.left + "px";
            oBox.style.top = boxPoint.top + "px";
        }

        // 鼠标松开以后，move事件不再执行
        document.onmouseup = function () {
            // 清除事件 只需要给事件赋值为null即可
            document.onmousemove = null;
            //松开的时候页面上不允许有事件残留，所以把up事件也清了，让再次按下鼠标 就又绑定上去了在·
            document.onmouseup = null;
        }

    }
</script>
</body>
</html>
```

#### 02.方法2
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>拖拽方法二</title>
    <link rel="stylesheet" href="./reset.css">
    <style>
        #box{
            width: 100px;
            height: 100px;
            background-color: red;
            position: absolute;
            left: 0;
            top: 0;
        }
    </style>
</head>
<body>
<div id="box">

</div>
<script src="./my.js"></script>
<script>
    var oBox = my.getID("box");
    // 对obox绑定鼠标按下事件
    oBox.onmousedown = function (ev) {
        var ev = ev ||window.event;
        // 获取按下的时候鼠标的位置
        var mouseDown = {
            left:ev.clientX,
            top:ev.clientY
        }
        // 获取按下的时候 元素的距离左边缘和上边缘的位置
        var oBoxToDoc = {
            left:my.getEleToDoc(oBox).left,
            top:my.getEleToDoc(oBox).top
        }
        console.log(mouseDown)
        document.onmousemove = function(ev){
            var ev = ev || window.event;
            //最终鼠标的位置用对象来保存
            var boxPoint = {
                left:ev.clientX - mouseDown.left + oBoxToDoc.left,
                top:ev.clientY - mouseDown.top + oBoxToDoc.top
            }
            //赋值
            oBox.style.left = boxPoint.left + "px";
            oBox.style.top = boxPoint.top + "px";
        }

        // 鼠标松开以后，move事件不再执行
        document.onmouseup = function () {
            // 清除事件 只需要给事件赋值为null即可
            document.onmousemove = null;
            //松开的时候页面上不允许有事件残留，所以把up事件也清了，让再次按下鼠标 就又绑定上去了在·
            document.onmouseup = null;
        }

    }
</script>
</body>
</html>
```

#### 03.方法3
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>拖拽方法三</title>
    <link rel="stylesheet" href="./reset.css">
    <style>
        #box{
            width: 100px;
            height: 100px;
            background-color: red;
            position: absolute;
            left: 0;
            top: 0;
        }
    </style>
</head>
<body>
<div id="box">

</div>
<script src="./my.js"></script>
<script>
    var oBox = my.getID("box");
    // 对obox绑定鼠标按下事件
    oBox.onmousedown = function (ev) {
        var ev = ev ||window.event;
        // 获取鼠标距离当前元素边缘的距离
        var mouseDown = {
            left:my.getOffset(ev,oBox).left,
            top:my.getOffset(ev,oBox).top
        }
        document.onmousemove = function(ev){
            var ev = ev || window.event;
            //最终鼠标的位置用对象来保存
            var boxPoint = {
                left:ev.clientX - mouseDown.left,
                top:ev.clientY - mouseDown.top
            }
            //赋值
            oBox.style.left = boxPoint.left + "px";
            oBox.style.top = boxPoint.top + "px";
        }

        // 鼠标松开以后，move事件不再执行
        document.onmouseup = function () {
            // 清除事件 只需要给事件赋值为null即可
            document.onmousemove = null;
            //松开的时候页面上不允许有事件残留，所以把up事件也清了，让再次按下鼠标 就又绑定上去了在·
            document.onmouseup = null;
        }

    }
</script>
</body>
</html>
```
#### 04.拖拽临界值
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>拖拽方法三</title>
    <link rel="stylesheet" href="./reset.css">
    <style>
        #box{
            width: 100px;
            height: 100px;
            background-color: red;
            position: absolute;
            left: 0;
            top: 0;
        }
    </style>
</head>
<body>
<div id="box">

</div>
<script src="./my.js"></script>
<script>
    var oBox = my.getID("box");
    // 对obox绑定鼠标按下事件
    oBox.onmousedown = function (ev) {
        var ev = ev ||window.event;
        // 获取鼠标距离当前元素边缘的距离
        var mouseDown = {
            left:my.getOffset(ev,oBox).left,
            top:my.getOffset(ev,oBox).top
        }
        document.onmousemove = function(ev){
            var ev = ev || window.event;
            //最终鼠标的位置用对象来保存
            var boxPoint = {
                left:ev.clientX - mouseDown.left,
                top:ev.clientY - mouseDown.top
            }

            // 在赋值之前 判断临界值
            if (boxPoint.left <= 0){
                boxPoint.left = 0;
            }else if (boxPoint.left >= my.getScreen().width - oBox.offsetWidth){
                boxPoint.left = my.getScreen().width - oBox.offsetWidth;
            }
            if (boxPoint.top <= 0){
                boxPoint.top = 0;
            }else if (boxPoint.top >= my.getScreen().height - oBox.offsetHeight){
                boxPoint.top = my.getScreen().height - oBox.offsetHeight;
            }




            //赋值
            oBox.style.left = boxPoint.left + "px";
            oBox.style.top = boxPoint.top + "px";
        }

        // 鼠标松开以后，move事件不再执行
        document.onmouseup = function () {
            // 清除事件 只需要给事件赋值为null即可
            document.onmousemove = null;
            //松开的时候页面上不允许有事件残留，所以把up事件也清了，让再次按下鼠标 就又绑定上去了在·
            document.onmouseup = null;
        }

    }
</script>
</body>
</html>
```

### 14.键盘事件
- 当用户操作键盘的时候会触发键盘事件
- keydown：键盘被按下某个按键的时候触发，如果按住某一个按键，会不断触发该事件
- keyup：释放某一个按键的时候触发。不是持续相应状态
```js
    document.onkeydown = function (e) {
        var e = e || window.event;
        console.log(e);
    }
```

### 15.键盘事件属性
- 键盘事件定义了很多属性
- keyCode：对应键盘中对应键位的键值
- shiftKey、ctrlKey、altKey是否按下shift strl alt按键  返回布尔值
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>键码</title>
</head>
<body>
Jintiantianqizhenhao
<script>
    document.onkeypress = function (ev) {
        /*var ev = ev || window.event;
        // console.log(ev)
        if (ev.keyCode == 67 && ev.ctrlKey) {
            alert("你又来复制了？");
        }

        return false;*/
        console.log(1);
    }
</script>
</body>
</html>

```

### 16.敲回车 阻止提交表单
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>敲回车 阻止提交表单</title>
</head>
<body>
<form action="http://www.baidu.com">
    <input type="text" id="ipt">
    <button id="btn">提交</button>
</form>

<script>
var oIpt = document.getElementById("ipt");
oIpt.onkeydown = function (ev) {
    var ev = ev || window.event;
    if (ev.keyCode == 13){
        alert("你又敲回车了")

        return false;
    }
}
</script>
</body>
</html>
```

### 17.键盘控制移动
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>键盘控制移动</title>
    <style>
        #box{
            width: 100px;
            height: 100px;
            background-color: red;
            position: absolute;
            left: 0;
            top: 0;
        }
    </style>
</head>
<body>
<div id="box">

</div>
<script>
    var oBox = document.getElementById("box");
    /*document.onkeydown = function (ev) {
        // console.log(1);
        var ev = ev || window.event;
        if(ev.keyCode == 39){
            oBox.style.left = oBox.offsetLeft + 1 + 'px';
        }
        if(ev.keyCode == 38){
            oBox.style.top = oBox.offsetTop - 1 + 'px';
        }
        if(ev.keyCode == 37){
            oBox.style.left = oBox.offsetLeft - 1 + 'px';
        }
        if(ev.keyCode == 40){
            oBox.style.top = oBox.offsetTop + 1 + 'px';
        }
    }*/

    var shang = false,xia = false,zuo = false,you = false;
    var x = 0,y = 0;
    document.onkeydown = function (ev) {
        var ev = ev || window.event;
        /*if (ev.keyCode == 38){
            shang = true;
        }
        if (ev.keyCode == 39){
            you = true;
        }
        if (ev.keyCode == 40){
            xia = true;
        }
        if (ev.keyCode == 37){
            zuo = true;
        }*/

        switch (ev.keyCode){
            case 38:
                shang = true;
                break;
            case 39:
                you = true;
                break;
            case 40:
                xia = true;
                break;
            case 37:
                zuo = true;
                break;
        }
    }
    document.onkeyup = function (ev){
        var ev = ev || window.event;
        switch (ev.keyCode){
            case 38:
                shang = false;
                break;
            case 39:
                you = false;
                break;
            case 40:
                xia = false;
                break;
            case 37:
                zuo = false;
                break;
        }
    }
    timer = setInterval(function () {
        if (shang){
            y --;
        }
        if(xia){
            y ++;
        }
        if (zuo) {
            x --;
        }
        if(you){
            x ++;
        }

        oBox.style.top = y + "px";
        oBox.style.left = x + "px";
    },10)
</script>
</body>
</html>
```

### 18.敲回车提交表单
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>06.敲回车提交表单</title>
</head>
<body>
<form id="form" action="http://www.baidu.com">
    请输入手机号
    <input type="text" id="ipt">
</form>
<script>
    /*
        当用户输入完成敲击回车按键的时候。如果用户输入的都是11为纯数字  那么就让用户提交  否则不提交
     */
    var oForm = document.getElementById("form");
    var oIpt = document.getElementById("ipt");

    // 我们一般提交表单的时候，判断比较复杂 ，基本不会使用默认的跳转  而是我们主动跳转
    // 所以一般在提交事件中，首先阻止默认事件
    oIpt.onkeydown = function (ev) {
        var ev = ev || window.event;
        // ev.preventDefault?ev.preventDefault():ev.returnValue = false;

        if (ev.keyCode == 13){
            if (this.value.length == 11 && !isNaN(this.value)) {
                alert("输入正确");
                // 手动让表单提交  可以让form调用submit方法
                oForm.submit();
            }else{
                alert("重新输入");
                // ev.preventDefault?ev.preventDefault():ev.returnValue = false;
                return false;
            }
        }

    }
</script>
</body>
</html>
```


### 19.事件委托引入
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>事件委托</title>
</head>
<body>
<button id="btn">
    添加一个新元素
</button>
<ul id="box">
    <li>11</li>
    <li>22</li>
    <li>33</li>
    <li>44</li>
    <li>55</li>
</ul>
<script>
    var oBtn = document.getElementById("btn");
    var oBox = document.getElementById("box");
    var oLis = oBox.getElementsByTagName("li");

    for (var i = 0; i <oLis.length ; i++) {
        oLis[i].onclick = function () {
            this.style.backgroundColor = "red";
        }
    }
    
    oBtn.onclick = function () {
        var newLi = document.createElement("li");
        newLi.innerHTML = "newLi";
        oBox.appendChild(newLi);


        /*newLi.onclick = function () {
            this.style.backgroundColor = "red";
        }*/

        /*for (var i = 0; i <oLis.length ; i++) {
            oLis[i].onclick = function () {
                this.style.backgroundColor = "red";
            }
        }*/
    }
</script>
</body>
</html>
```

### 20.事件委托
- 事件委托（delegate） 也称为事件托管或者事件代理，就是把目标节点的事件绑定到祖先的节点上
- 这种简单而优雅的事件注册方式是给予事件传播过程中，逐层冒泡总能被祖先元素捕捉到
- 优点：优化代码提升性能，把html和js分离，防止动态添加或删除节点中注册事件的丢失现象
```html
<!DOCTYPE html>
<html lang="en">
<head> 
    <meta charset="UTF-8">
    <title>事件委托</title>
</head>
<body>
<button id="btn">
    添加一个新元素
</button>
<ul id="box">
    <li>11</li>
    <li>22</li>
    <li>33</li>
    <li>44</li>
    <li>55</li>
</ul>
<script>
    var oBtn = document.getElementById("btn");
    var oBox = document.getElementById("box");
    var oLis = oBox.getElementsByTagName("li");


    /*事件委托的优点：
        1、可以对未来的元素绑定事件
        2、避免使用for循环 提高效率*/
    // 事件委托的原理：冒泡
    oBox.onclick = function (ev) {
        var ev = ev || window.event;
        // ev.target当前时间精确发生的元素
        console.log(ev.target);

        // 在这里this仍然是指向oBox
        // this.style.backgroundColor = "red";

        // 给精确的元素绑定点击事件，但是没有判断   所有元素都能触发
        // ev.target.style.backgroundColor = "red";

        if (ev.target.nodeName.toLowerCase() == "li" ){
            ev.target.style.backgroundColor = "red";
        }
    }


    oBtn.onclick = function () {
        var newLi = document.createElement("li");
        newLi.innerHTML = "newLi";
        oBox.appendChild(newLi);
    }
</script>
</body>
</html>
```

### 21.选择城市
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>选择城市</title>
    <link rel="stylesheet" href="./reset.css">
    <style>
        #outer{
            width: 400px;
            margin:20px auto;
        }
        #con{
            position: relative;
        }
        #select{
            height: 40px;
            background-color: grey;
            line-height: 40px;
        }
        #cityList{
            overflow: hidden;
            width: 400px;
            position: absolute;
            background-color: red;
            display: none;
        }
        #cityList li{
            width: 80px;
            text-align: center;
            margin: 10px;
            float: left;
        }
    </style>
</head>
<body>
<div id="outer">
    <h2 id="title">深圳</h2>
    <div id="con">
        <p id="select">点击我选择城市</p>
        <ul id="cityList">
            <li>深圳</li>
            <li>北京</li>
            <li>广州</li>
            <li>上海</li>
            <li>长沙</li>
            <li>南昌</li>
            <li>武汉</li>
            <li>焦作</li>
            <li>郑州</li>
            <li>太原</li>
            <li>草围</li>
        </ul>
    </div>
</div>
<script>
    var oCityList = document.getElementById("cityList");
    var oTitle = document.getElementById("title");
    document.onclick = function (ev) {
        var ev = ev || window.event;
        /*在现代浏览器中直接使用  ev.target
        在ie678中  使用 window.target.srcElement; */
        var target = ev.target || target.srcElement;
        if (target.id == "select"){
            oCityList.style.display = "block";
            return;
        }
        if(target.nodeName == "LI" && target.parentNode.id == "cityList"){
            oCityList.style.display = "none";
            oTitle.innerHTML = target.innerHTML;
            return;
        }
        oCityList.style.display = "none";
    }
</script>
</body>
</html>
```

### 21.放大镜
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        *{
            margin: 0;
            padding: 0;
        }
        .box{
            position: relative;
        }
        .minbox{
            width: 200px;
            height: 200px;
            border: 1px solid #000;
            position: relative;
            float: left;
        }
        .minbox img{
            width: 200px;
            height: 200px;
        }
        .minbox .mask{
            width: 80px;
            height: 80px;
            background: rgba(22,45,116,.5);
            position: absolute;
            left: 20px;
            top: 0;
            display: none;
        }
        .maxbox{
            position: absolute;
            left: 202px;
            top: 0;
            width: 280px;
            height: 280px;
            overflow: hidden;
            display: none;
        }
        .maxbox img{
            width: 500px;
            height: 500px;
        }
    </style>
</head>
<body>
<div class="box">
    <div class="minbox">
        <img src="../images/01.jpg" alt="">
        <p class="mask"></p>
    </div>
    <div class="maxbox">
        <img src="../images/01.jpg" alt="">
    </div>
</div>
<script>
    var oMask = document.querySelector(".mask");
    var oMinImg = document.querySelector(".minbox img");
    var oMinBox = document.querySelector(".minbox");
    var oMaxImg = document.querySelector(".maxbox img");
    var oMaxBox = document.querySelector(".maxbox");

    oMinBox.onmouseenter = function () {
        oMask.style.display = "block";
        oMaxBox.style.display = "block";
        oMinBox.onmousemove = function (e) {
            var maskPoint = {
                left:e.clientX - this.getBoundingClientRect().left - oMask.offsetWidth/ 2,
                top:e.clientY - this.getBoundingClientRect().left - oMask.offsetHeight / 2
            }
            if(maskPoint.left <= 0){
                maskPoint.left = 0;
            }else if(maskPoint.left >= oMinBox.clientWidth - oMask.offsetWidth){
                maskPoint.left = oMinBox.clientWidth - oMask.offsetWidth
            }
            if(maskPoint.top <= 0){
                maskPoint.top = 0;
            }else if(maskPoint.top >= oMinBox.clientHeight - oMask.offsetHeight){
                maskPoint.top = oMinBox.clientHeight - oMask.offsetHeight
            }
            oMask.style.left = maskPoint.left + "px";
            oMask.style.top = maskPoint.top + "px";

            var scale = (oMinImg.offsetWidth - oMask.offsetWidth) / (oMaxImg.offsetWidth - oMaxBox.offsetWidth);
            var maxImgPoint = {
                left: maskPoint.left / scale,
                top:maskPoint.top / scale
            }
            oMaxImg.style.marginLeft = - maxImgPoint.left + "px";
            oMaxImg.style.marginTop = - maxImgPoint.top + "px";
        }
        oMinBox.onmouseleave = function () {
            oMask.style.display = "none";
            oMaxBox.style.display = "none";
            oMinBox.onmousemove = null;
            oMinBox.onmouseleave = null;
        }
    }

</script>
</body>
</html>
```

### 22.getBoundingClientRect
- obj.getBoundingClientRect用于获取某个元素相对于视窗的位置集合。集合中有top, right, bottom, left等属性
- rectObject.top：元素上边到视窗上边的距离;
- rectObject.right：元素右边到视窗左边的距离;
- rectObject.bottom：元素下边到视窗上边的距离;
- rectObject.left：元素左边到视窗左边的距离;
- ie9以上支持width/height属性。

### 23.自定义滚动条
#### 01.滑块
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>滚动条基础版</title>
    <link rel="stylesheet" href="./reset.css">
    <style>
        /*禁止系统滚动条*/
        html,body{
            width: 100%;
            height: 100%;
            overflow: hidden;
        }
        #wrap{
            width: 40px;
            height: 100%;
            position: absolute;
            right: 0;
            top: 0;
            background-color: #5ab3f4;
        }
        #inner{
            width: 40px;
            height: 50px;
            position: absolute;
            top: 0;
            left: 0;
            background-color: #ff7b86;
        }
    </style>
</head>
<body>
<!--页面的内容区域-->
<div id="content">

</div>
<div id="wrap">
<!--    小滑块-->
    <div id="inner">

    </div>
</div>
<script src="./my.js"></script>
<script>
    var oCon = my.getID("content");
    var oWrap = my.getID("wrap");
    var oInner = my.getID("inner");

    // 自动生成内容
    var con = "";
    for (var i = 0; i < 1000; i++) {
        con += (i +"<br>");
        oCon.innerHTML = con;
    }


    oInner.onmousedown = function (ev) {
        var ev = ev || window.event;
        ev.preventDefault?ev.preventDefault():ev.returnValue = false;
        var mouseDownTop = ev.clientY;
        var innerStart = my.getEleToDoc(oInner).top;
        document.onmousemove = function (ev) {
            var ev = ev || window.event;
            ev.preventDefault?ev.preventDefault():ev.returnValue = false;
            var innerPointY = ev.clientY - mouseDownTop + innerStart;

            if (innerPointY < 0){
                innerPointY = 0;
            } else if (innerPointY >= oWrap.clientHeight - oInner.offsetHeight){
                innerPointY = oWrap.clientHeight - oInner.offsetHeight;
            }
            oInner.style.top = innerPointY + "px";
        }
        document.onmouseup = function () {
            document.onmouseup = document.onmousemove = null;
        }
    }
</script>
</body>
</html>
```

#### 02.禁止系统滚动条
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <link rel="stylesheet" href="./reset.css">
    <style>
        html{
            width: 700px;
            height: 400px;
            margin: 10px auto;
            /*background-color: yellow;*/
            border:1px solid #000;
            overflow: hidden;
        }
        body{
            width: 400px;
            height: 300px;
            margin: 30px auto;
            /*background-color: pink;*/
            border:1px solid green;
            /*overflow: scroll;*/
            overflow: hidden;
        }
        /*当body和html
            只有body有overflow属性 那么body的滚动条会传递到系统滚动条

            只有html有overflow属性 那么body的滚动条会传递到系统滚动条

            当两个都有overflow属性的时候，body的滚动条就是自己的
            */

        /*系统的滚动条就是body和html的滚动条传递上去的
        所以把html和body的overflow设置为隐藏  那么系统滚动条就没有来源
        所就禁止了系统滚动条*/
        .box{
            height: 4000px;
            width: 300px;
            background-color: red;
        }
    </style>
</head>
<body>
    <div class="box"></div>

</body>
</html>
```

#### 03.内容移动初级版本
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>滚动条基础版</title>
    <link rel="stylesheet" href="./reset.css">
    <style>
        /*禁止系统滚动条*/
        html,body{
            width: 100%;
            height: 100%;
            overflow: hidden;
        }
        #wrap{
            width: 40px;
            height: 100%;
            position: absolute;
            right: 0;
            top: 0;
            background-color: #5ab3f4;
        }
        #inner{
            width: 40px;
            height: 50px;
            position: absolute;
            top: 0;
            left: 0;
            background-color: #ff7b86;
        }
        #content{
            position: absolute;
            left: 0;
            top: 0;
        }
    </style>
</head>
<body>
<!--页面的内容区域-->
<div id="content">

</div>
<div id="wrap">
<!--    小滑块-->
    <div id="inner">

    </div>
</div>
<script src="./my.js"></script>
<script>
    var oCon = my.getID("content");
    var oWrap = my.getID("wrap");
    var oInner = my.getID("inner");

    // 自动生成内容
    var con = "";
    for (var i = 0; i < 300; i++) {
        con += (i +"<br>");
        oCon.innerHTML = con;
    }


    oInner.onmousedown = function (ev) {
        var ev = ev || window.event;
        ev.preventDefault?ev.preventDefault():ev.returnValue = false;
        var mouseDownTop = ev.clientY;
        var innerStart = my.getEleToDoc(oInner).top;
        document.onmousemove = function (ev) {
            var ev = ev || window.event;
            ev.preventDefault?ev.preventDefault():ev.returnValue = false;
            var innerPointY = ev.clientY - mouseDownTop + innerStart;

            if (innerPointY < 0){
                innerPointY = 0;
            } else if (innerPointY >= oWrap.clientHeight - oInner.offsetHeight){
                innerPointY = oWrap.clientHeight - oInner.offsetHeight;
            }
            oInner.style.Matop = innerPointY + "px";

            // 计算比例
            var scale = innerPointY / (oWrap.clientHeight - oInner.offsetHeight);

            // 给content的top赋值
            console.log(oCon.offsetHeight);
            oCon.style.marginTop = - scale * (oCon.offsetHeight - my.getScreen().height) + "px";
        }
        document.onmouseup = function () {
            document.onmouseup = document.onmousemove = null;
        }
    }
</script>
</body>
</html>
```

#### 04.滑块高度比例版本
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>滚动条基础版</title>
    <link rel="stylesheet" href="./reset.css">
    <style>
        /*禁止系统滚动条*/
        html,body{
            width: 100%;
            height: 100%;
            overflow: hidden;
        }
        #wrap{
            width: 40px;
            height: 100%;
            position: absolute;
            right: 0;
            top: 0;
            background-color: #5ab3f4;
        }
        #inner{
            width: 40px;
            position: absolute;
            top: 0;
            left: 0;
            background-color: #ff7b86;
        }
        #content{
            position: absolute;
            left: 0;
            top: 0;
        }
    </style>
</head>
<body>
<!--页面的内容区域-->
<div id="content">

</div>
<div id="wrap">
<!--    小滑块-->
    <div id="inner">

    </div>
</div>
<script src="./my.js"></script>
<script>
    var oCon = my.getID("content");
    var oWrap = my.getID("wrap");
    var oInner = my.getID("inner");

    // 自动生成内容
    var con = "";
    for (var i = 0; i < 30; i++) {
        con += (i +"<br>");
        oCon.innerHTML = con;
    }

    // 计算滑块的高度
    var scale = my.getScreen().height / oCon.offsetHeight;
    oInner.style.height = scale * oWrap.offsetHeight + "px";


    oInner.onmousedown = function (ev) {
        var ev = ev || window.event;
        ev.preventDefault?ev.preventDefault():ev.returnValue = false;
        var mouseDownTop = ev.clientY;
        var innerStart = my.getEleToDoc(oInner).top;
        document.onmousemove = function (ev) {
            var ev = ev || window.event;
            ev.preventDefault?ev.preventDefault():ev.returnValue = false;
            var innerPointY = ev.clientY - mouseDownTop + innerStart;

            if (innerPointY < 0){
                innerPointY = 0;
            } else if (innerPointY >= oWrap.clientHeight - oInner.offsetHeight){
                innerPointY = oWrap.clientHeight - oInner.offsetHeight;
            }
            oInner.style.top = innerPointY + "px";

            // 计算比例
            var scale = innerPointY / (oWrap.clientHeight - oInner.offsetHeight);

            // 给content的top赋值
            console.log(oCon.offsetHeight);
            oCon.style.top = - scale * (oCon.offsetHeight - my.getScreen().height) + "px";
        }
        document.onmouseup = function () {
            document.onmouseup = document.onmousemove = null;
        }
    }
</script>
</body>
</html>
```

#### 05.比例版本
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>滚动条基础版</title>
    <link rel="stylesheet" href="./reset.css">
    <style>
        /*禁止系统滚动条*/
        html,body{
            width: 100%;
            height: 100%;
            overflow: hidden;
        }
        #wrap{
            width: 40px;
            height: 100%;
            position: absolute;
            right: 0;
            top: 0;
            background-color: #5ab3f4;
        }
        #inner{
            width: 40px;
            position: absolute;
            top: 0;
            left: 0;
            background-color: #ff7b86;
        }
        #content{
            position: absolute;
            left: 0;
            top: 0;
        }
    </style>
</head>
<body>
<!--页面的内容区域-->
<div id="content">

</div>
<div id="wrap">
<!--    小滑块-->
    <div id="inner">

    </div>
</div>
<script src="./my.js"></script>
<script>
    var oCon = my.getID("content");
    var oWrap = my.getID("wrap");
    var oInner = my.getID("inner");

    // 自动生成内容
    var con = "";
    for (var i = 0; i < 100; i++) {
        con += (i +"<br>");
        oCon.innerHTML = con;
    }

    // 计算滑块的高度
    var scale = my.getScreen().height / oCon.offsetHeight;
    oInner.style.height = scale * oWrap.offsetHeight + "px";

    
    oInner.onmousedown = function (ev) {
        var ev = ev || window.event;
        ev.preventDefault?ev.preventDefault():ev.returnValue = false;
        var mouseDownTop = ev.clientY;
        var innerStart = my.getEleToDoc(oInner).top;
        document.onmousemove = function (ev) {
            var ev = ev || window.event;
            ev.preventDefault?ev.preventDefault():ev.returnValue = false;
            var innerPointY = ev.clientY - mouseDownTop + innerStart;

            if (innerPointY < 0){
                innerPointY = 0;
            } else if (innerPointY >= oWrap.clientHeight - oInner.offsetHeight){
                innerPointY = oWrap.clientHeight - oInner.offsetHeight;
            }
            oInner.style.top = innerPointY + "px";

            oCon.style.top = - innerPointY / scale + "px";
        }
        document.onmouseup = function () {
            document.onmouseup = document.onmousemove = null;
        }
    }
</script>
</body>
</html>
```

#### 06.滚轮事件
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        #box{
            width: 300px;
            height: 300px;
            background-color: red;
        }
    </style>
</head>
<body>
<div id="box">

</div>
<script>
    // 滚轮事件
    /*
    ie/谷歌：
    onmousewheel(DOM0事件)
        ev.wheelDelta
            上：120
            下：-120

    火狐：
    DOMMouseScroll（Dom2级事件）
        ev.detail
            上：-3
            下：3

     */

    // 滚动滚轮让元素变大变小
    var oBox = document.getElementById("box");
    var x = 300;

    function mouseScroll(ev){
        var ev = ev || window.event;
        if (ev.wheelDelta) {
            if (ev.wheelDelta > 0){
                x -=5;
            }else{
                x +=5;
            }
        }else{
            if (ev.detail < 0) {
                x -= 5;
            }else{
                x += 5;
            }
        }

        oBox.style.height = x + "px";

    }
    oBox.onmousewheel = mouseScroll;
    oBox.addEventListener("DOMMouseScroll",mouseScroll);

   /* oBox.onmousewheel = function (ev) {
        var ev = ev || window.event;
        console.log(ev.wheelDelta)
        if (ev.wheelDelta > 0){
            x -=5;
        }else{
            x +=5;
        }
        oBox.style.height = x + "px";
    }

    oBox.addEventListener("DOMMouseScroll",function (ev) {
           if (ev.detail < 0) {
               x -= 5;
           }else{
               x += 5;
           }
            oBox.style.height = x + "px";
    })*/
</script>
</body>
</html>
```

#### 07.自定义滚轮版本
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>滚动条基础版</title>
    <link rel="stylesheet" href="./reset.css">
    <style>
        /*禁止系统滚动条*/
        html,body{
            width: 100%;
            height: 100%;
            overflow: hidden;
        }
        #wrap{
            width: 40px;
            height: 100%;
            position: absolute;
            right: 0;
            top: 0;
            background-color: #5ab3f4;
        }
        #inner{
            width: 40px;
            position: absolute;
            top: 0;
            left: 0;
            background-color: #ff7b86;
        }
        #content{
            position: absolute;
            left: 0;
            top: 0;
        }
    </style>
</head>
<body>
<!--页面的内容区域-->
<div id="content">

</div>
<div id="wrap">
<!--    小滑块-->
    <div id="inner">

    </div>
</div>
<script src="./my.js"></script>
<script>
    var oCon = my.getID("content");
    var oWrap = my.getID("wrap");
    var oInner = my.getID("inner");

    // 自动生成内容
    var con = "";
    for (var i = 0; i < 100; i++) {
        con += (i +"<br>");
        oCon.innerHTML = con;
    }

    // 计算滑块的高度
    var scale = my.getScreen().height / oCon.offsetHeight;
    oInner.style.height = scale * oWrap.offsetHeight + "px";

    
    oInner.onmousedown = function (ev) {
        var ev = ev || window.event;
        ev.preventDefault?ev.preventDefault():ev.returnValue = false;
        var mouseDownTop = ev.clientY;
        var innerStart = my.getEleToDoc(oInner).top;
        document.onmousemove = function (ev) {
            var ev = ev || window.event;
            ev.preventDefault?ev.preventDefault():ev.returnValue = false;
            var innerPointY = ev.clientY - mouseDownTop + innerStart;

            if (innerPointY < 0){
                innerPointY = 0;
            } else if (innerPointY >= oWrap.clientHeight - oInner.offsetHeight){
                innerPointY = oWrap.clientHeight - oInner.offsetHeight;
            }
            oInner.style.top = innerPointY + "px";

            oCon.style.top = - innerPointY / scale + "px";
        }
        document.onmouseup = function () {
            document.onmouseup = document.onmousemove = null;
        }
    }


    document.onmousewheel = mouseScroll;
    document.addEventListener("DOMMouseScroll",mouseScroll);
    function mouseScroll(ev){
        var ev = ev || window.event;

        var x = oInner.offsetTop;
        if (ev.wheelDelta) {
            if (ev.wheelDelta > 0){
                x -=5;
            }else{
                x +=5;
            }
        }else{
            if (ev.detail < 0) {
                x -= 5;
            }else{
                x += 5;
            }
        }
        console.log(x)

        if (x <= 0){
            x = 0;
        } else if(x >= oWrap.clientHeight - oInner.offsetHeight){
            x = oWrap.clientHeight - oInner.offsetHeight
        }

        oInner.style.top = x + "px";

        oCon.style.top = - x/scale + "px"
    }


</script>
</body>
</html>
```


## 补充：
### 01.监测网络

### 02. 

### 03.favicon设置
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <link rel="icon" href="../images/favicon.ico">
</head>
<body>
<!--http://cn.faviconico.org/  转换成ico图标-->

favicon.ico一般用于作为缩略的网站标志，它显示在浏览器的地址栏、浏览器标签上或者在收藏夹上，是展示网站个性的缩略logo标志，也可以说是网站头像,目前主要的浏览器都支持favicon.ico图标，

<!--引入有很多种方法-->
<!--有一种是前端引入的-->

1、最好使用ico格式，兼容性好。
2、比如在服务器环境下才能使用
</body>
</html>
```

### 04.复制文字
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>复制文字</title>
    <style>
        .copy{
            position: relative;
        }
        input{
            width: 1px;
            height: 1px;
            border: none;
            padding: 0;
            position: absolute;
            opacity: 0;
        }
    </style>
</head>
<body>
    <div class="copy">
        <p id="con">今天天气真好,课间有65个人在睡觉</p>
        <input type="text" id="ipt" value="">
    </div>
    <button id="btn">复制当前文字</button>
    <script>
        var oCopy = document.querySelector(".copy");
        var oCon = document.querySelector("#con");
        var oBtn = document.querySelector("#btn");
        var oIpt = document.querySelector("#ipt");
        // 点击复制 必须依赖于输入框元素  我们提供的复制方法 只能复制表单的value值
        // 所以我们需要把要复制的文字放入表单中，然后复制
        oBtn.onclick = function () {
            oIpt.value = oCon.innerHTML;
            oIpt.select();
            document.execCommand("copy")
        }
    </script>
</body>
</html>
```

### 05.复制文字封装
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>复制文字</title>
    <style>

    </style>
</head>
<body>
    <div class="copy">
        <p id="con">今天天气真好,课间有11个人在睡觉</p>
    </div>
    <button id="btn">复制当前文字</button>
    <script>
        var oCopy = document.querySelector(".copy");
        var oCon = document.querySelector("#con");
        var oBtn = document.querySelector("#btn");
        var oIpt = document.querySelector("#ipt");
        // 点击复制 必须依赖于输入框元素  我们提供的复制方法 只能复制表单的value值
        // 所以我们需要把要复制的文字放入表单中，然后复制
        oBtn.onclick = function () {
            /*//1、复制依赖表单，为了不影响结构，动态创建input
            var newInput = document.createElement("input");
            ///2、把新创建的input插入到页面中
            oCopy.appendChild(newInput);
            ///3、将要复制的内容 给到 input的value中
            newInput.value = oCon.innerHTML;
            // 4、选中当前表单的内容
            newInput.select();
            //5、调用document 的 execCommand方法的复制功能，就复制到剪切板了
            document.execCommand("copy")
            //6、用完input 就直接给删除就可以
            oCopy.removeChild(newInput);*/

            copyEleText(oCon);
        }

        // 复制封装函数

        function copyEleText(obj) {
            //1、复制依赖表单，为了不影响结构，动态创建input
            var newInput = document.createElement("input");
            ///2、把新创建的input插入到页面中  插入到obj的父级即可 不影响复制
            obj.parentNode.appendChild(newInput);
            ///3、将要复制的内容 给到 input的value中
            newInput.value = obj.innerHTML;
            // 4、选中当前表单的内容
            newInput.select();
            //5、调用document 的 execCommand方法的复制功能，就复制到剪切板了
            document.execCommand("copy")
            //6、用完input 就直接给删除就可以
            obj.parentNode.removeChild(newInput);
            alert("复制成功");
        }
    </script>
</body>
</html>
```

### 06.基本包装类型
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>基本包装类型</title>
</head>
<body>
<script>
    /*js的数据类型：基本类型值和引用类型值
        基本类型值：null  undefined string number  boolean
        引用类型值：objebct Array Date RegExp  Function*/


    // 1、其中基本类型值中  string  number boolean 被称作为基本包装类型

    // var str = "123";
    // var str = new String("123");

    // 2、string  number boolean都有自己的包装对象，包装对象其实就是对象，拥有属性和方法，
    // 这些属性和方法都是从String对象来的


    // 案例：以string举例子：
    var str = "hello world";
    var newArr = str.split("");

    // 以上代码在内部的操作如下：
        //1、找到相对应的包装对象类型，然后通过这个包装对象创建一个和str一样的值
        var _str = new String("hello world");
        //2、让_str来调用 方法 并返回出去
        var newArr = _str.split("");
        // 3、刚才临时创建的 用来调用方法的临时对象 被删除掉
        _str = null;




    // 为什么我们不能给基本类型扩展属性或方法
    var str = "1234444";
    str.name = "hello";
    // 解析如下：
        var _str = new String("1234444");
        _str.name = "hello";
        _str = null;
</script>
</body>
</html>
```





























