### 会话控制

### 会话控制是什么

HTTP协议是一个无状态的协议，它无法区分多次请求是否发送自同一客户端。

而我们在实际的使用中，却又大量的这种需求，我们需要通过会话的控制来解决该问题。

### cookie是什么

cookie本质是一个存储在浏览器的文本，随着http请求自动传递给服务器。

也可以说cookie是一个头（请求头/响应头）：

服务器以响应头的形式将Cookie发送给浏览器

浏览器收到以后会自动将Cookie保存

浏览器再次访问服务器时，会以请求头的形式将Cookie发回

服务器就可以通过检查浏览器发回的Cookie来识别出不同的浏览器

浏览器第一次访问的时候是没有Cookie的;响应头内容不可以有==中文==

### cookie的不足

各个浏览器对cookie的数量和大小都有不同的限制，这样就导致我们不能在Cookie中保存过多的信息。一般数量不超过50个，单个大小不超过4kb。

cookie是由服务器发送给浏览器，再由浏览器将cookie发回，如果cookie较大会导致发送速度非常慢，降低用户的体验。

### cookie的使用

通过配置cookie-parser中间件，可以将cookie解析为一个对象，并且添加为req的cookies属性，使用步骤：

1) 下载安装

```
npm i cookie-parser --save
```

2) 引入

```
var cookieParser = require("cookie-parser");
```

3) 设置为中间件

```
var cookieParser = require("cookie-parser");
```

4) 创建Cookie

```
res.cookie("username","sunwukong" , {maxAge:15000});
//设置一个有效期为1天的cookie maxAge单位是毫秒，可以设置多个cookie

res.cookie("username","sunwukong" , {maxAge:1000*60*60*24});
```

5) 删除Cookie

```
//可以通过通过使用一个立即失效的cookie来替换cookie的形式来删除cookie

res.cookie("username","11",{maxAge:0});

//用来删除一个cookie

res.clearCookie(“username”)用来删除一个指定cookie
```

#### 0-express框架

1)安装包

~~~
npm i express
~~~

2）引入express

```
const express=require("express");
```

3）创建应用对象

```
const app=express();
```

3）创建路由规则

```
app.get("/",(request,response)=>{
	//获取cookie
	console.log(request.cookies);
	response.end("hello express");
})
//路径不同走的位置就不一样
app.get("/admin",(request,response)=>{
	response.send("你好admin");
})
```
#### end 与send
两个都是用来设置响应体的
* end不会自动加字符集响应头  end只能是字符串和buffer
* send 会自动加字符集响应头   send可以设置多种类型 比如可以传json对象,Buffer,String,Array 


## session

### session是什么

Session 是一个对象，存储特定用户会话所需的属性及配置信息。

#### session运作流程

我们可以在服务器中为每一次会话创建一个对象，然后每个对象都设置一个唯一的id，并将该id以cookie的形式发送给浏览器，然后将会话中产生的数据统一保存到这个对象中，这样我们就可以将用户的数据全都保存到服务器中，而不需要保存到客户端，客户端只需要保存一个id即可。

### ***\*session的使用\***

1) 下载安装

```
npm i connect-mongo express-session --save
```

2) 引入模块

```
var session = require("express-session");
```



3) 设置为中间件

```js
app.use(session({
 name: 'id22',  //设置cookie的name，默认值是：connect.sid
 secret: 'atguigu', //参与加密的字符串（又称签名）
 saveUninitialized: false, //是否为每次请求都设置一个cookie用来存储session的id
 resave: true ,//是否在每次请求时重新保存session
 cookie: {
  httpOnly: true, // 开启后前端无法通过 JS 操作
  maxAge: 1000*30 // 这一条 是控制 sessionID 的过期时间的！！！
 },
}));
```





### ***\*cookie\**** ***\*和 session的区别\****

1) 存在的位置：

cookie 存在于客户端，  IE临时文件夹中

session 存在于服务器端，一个session域对象为一个用户浏览器服务

2) 安全性：

cookie是以明文的方式存放在客户端的，安全性低，可以通过一个加密算法进行加密后存放

session存放于服务器中，所以安全性好

3) 网络传输量：

cookie会传递消息给服务器

session本身存放于服务器，但是通过cookie传递id，会有少量的传送流量

4) 大小：

cookie 保存的数据不能超过4K，很多浏览器都限制一个站点最多保存50个cookie

session 保存数据理论上没有任何限制

 

 