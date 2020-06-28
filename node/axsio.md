axios从入门到源码分析

### 1.第1章：HTTP相关
#### 1.1.MDN文档
https://developer.mozilla.org/zh-CN/docs/Web/HTTP/Overview
#### 1.2.HTTP请求交互的基本过程

1.前台应用从浏览器端向服务器发送HTTP请求(请求报文)
2.后台服务器接收到请求后, 调度服务器应用处理请求, 向浏览器端返回HTTP响应(响应报文)
3.浏览器端接收到响应, 解析显示响应体/保存数据并调用监视回调

#### 1.3.HTTP请求报文
1.请求行:
method url
GET /product_detail?id=2
POST /login 
2.请求头(多个)
Host: www.baidu.com
Cookie: BAIDUID=AD3B0FA706E; BIDUPSID=AD3B0FA706;
Content-Type: application/x-www-form-urlencoded 或者 application/json
3.请求体
urlencoded格式: username=tom&pwd=123
json格式: {"username": "tom", "pwd": 123}
#### 1.4.HTTP响应报文
1.响应行:  
status statusText
200 OK
404 Not Found
2.响应头(多个)
Content-Type: text/html;charset=utf-8   text/json;charset=utf-8
Set-Cookie: BD_CK_SAM=1;path=/
3.响应体
html文本/json文本/js/css/图片...
#### 1.5.post请求体参数格式
1.Content-Type: application/x-www-form-urlencoded;charset=utf-8
用于键值对参数，参数的键值用=连接, 参数之间用&连接
例如: name=%E5%B0%8F%E6%98%8E&age=12
2.Content-Type: application/json;charset=utf-8
用于json字符串参数
例如: {"name": "%E5%B0%8F%E6%98%8E", "age": 12}
3.Content-Type: multipart/form-data
用于文件上传请求
#### 1.6.常见的响应状态码
200  OK                   请求成功。一般用于GET与POST请求
201  Created               已创建。成功请求并创建了新的资源
401  Unauthorized          未授权/请求要求用户的身份认证
404  Not Found             服务器无法根据客户端的请求找到资源
500  Internal Server Error     服务器内部错误，无法完成请求
#### 1.7.不同类型的请求及其作用
1.GET: 从服务器端读取数据
2.POST: 向服务器端添加新数据
3.PUT: 更新服务器端数据
4.PATCH: 更新服务器数据
5.DELETE: 删除服务器端数据

### 1.8.使用postman测试API

1.9.API的分类
1.9.1.REST(restful) API
1.发送请求进行CRUD哪个操作由请求方式来决定
2.同一个请求路径可以进行多个操作
3.请求方式会用到GET/POST/PUT/DELETE
1.9.2.非REST(restless) API
1.请求方式不决定请求的CRUD操作
2.一个请求路径只对应一个操作
3.一般只有GET/POST
#### 1.10.使用json-server搭建REST API
1.10.1.json-server是什么?
用来快速搭建模拟的REST API的工具包
1.10.2.使用json-server
1.在线文档: https://github.com/typicode/json-server
2.下载: npm install -g json-server
3.目标根目录下创建数据库json文件: db.json
        {
          "posts": [
            { "id": 1, "title": "json-server", "author": "typicode" }
          ],
          "comments": [
            { "id": 1, "body": "some comment", "postId": 1 }
          ],
          "profile": { "name": "typicode" }
        }
4.启动服务器执行命令: json-server --watch db.json
1.10.3.使用浏览器访问测试
http://localhost:3000/posts
http://localhost:3000/posts/1
1.10.4.使用postman测试接口
测试GET / POST / PUT / DELETE请求
### 2.第2章：XHR的理解和使用
#### 2.1.MDN文档
https://developer.mozilla.org/zh-CN/docs/Web/API/XMLHttpRequest
#### 2.2.理解
1.使用XMLHttpRequest (XHR)对象可以与服务器交互, 也就是发送ajax请求
2.前端可以获取到数据，而无需让整个的页面刷新。
3.这使得Web页面可以只更新页面的局部，而不影响用户的操作。

#### 2.3.区别一般http请求与ajax请求

1.ajax请求是一种特别的http请求
2.对服务器端来说, 没有任何区别, 区别在浏览器端
3.浏览器端发请求: 只有XHR或fetch发出的才是ajax请求, 其它所有的都是非ajax请求
4.浏览器端接收到响应
(1)一般请求: 浏览器一般会直接显示响应体数据, 也就是我们常说的刷新/跳转页面
(2)ajax请求: 浏览器不会对界面进行任何更新操作, 只是调用监视的回调函数并传入响应相关数据

#### 2.4.API
1.XMLHttpRequest(): 创建XHR对象的构造函数
2.status: 响应状态码值, 比如200, 404
3.statusText: 响应状态文本
4.readyState: 标识请求状态的只读属性
0:  初始
1:  open()之后
2:  send()之后
3:  请求中
4:  请求完成
5.onreadystatechange: 绑定readyState改变的监听
6.responseType: 指定响应数据类型, 如果是'json', 得到响应后自动解析响应体数据
7.response: 响应体数据, 类型取决于responseType的指定
8.timeout: 指定请求超时时间, 默认为0代表没有限制
9.ontimeout: 绑定超时的监听
10.onerror: 绑定请求网络错误的监听
11.open(): 初始化一个请求, 参数为: (method, url[, async])
12.send(data): 发送请求
13.abort(): 中断请求
14.getResponseHeader(name): 获取指定名称的响应头值
15.getAllResponseHeaders(): 获取所有响应头组成的字符串
16.setRequestHeader(name, value): 设置请求头
2.5.使用axios发ajax请求


#### 2.6.XHR的基本使用
1.创建XHR对象
2.打开连接
3.绑定状态改变的监听, 并在异步回调中读取响应数据
4.发送请求

#### 2.7.XHR的ajax封装(简单版axios)
2.7.1.特点
5.函数的返回值为promise, 成功的结果为response, 异常的结果为error
6.能处理多种类型的请求: GET/POST/PUT/DELETE
7.函数的参数为一个配置对象
{
url: '',   // 请求地址
method: '',   // 请求方式GET/POST/PUT/DELETE
params: {},  // GET/DELETE请求的query参数
data: {}, // POST或PUT请求的请求体参数 
}
8.响应json数据自动解析为js

#### 2.7.2 编码实现
```js
使用XHR封装发送ajax请求的通用函数
      返回值: promise
      参数为配置对象
        url: 请求地址
        params: 包含所有query请求参数的对象 {name: tom, age: 12} ==> name=tom&age=12
        data: 包含所有请求体参数数据的对象
        method: 为请求方式
    */
    function axios({url, method='GET', params={}, data={}}) {

      method = method || 'GET'
      method = method.toUpperCase()
      // 将params中的参数属性拼接到url上   
      // {name: tom: pwd: 123}  ===> queryStr=name=tom&pwd=123
      // url + ? + queryStr
      let queryStr = ''
      Object.keys(params).forEach(key => {
        // &pwd=123
          queryStr += '&' + key + '=' + params[key]
      })
      // '&name=tom&pwd=123' 或者 ''
      if (queryStr) {
        queryStr = queryStr.substring(1) // 'name=tom&pwd=123'
        url += '?' + queryStr  // /user?name=tom&pwd=123
      }
      
      return new Promise((resolve, reject) => {
        // 创建XHR对象
        const request = new XMLHttpRequest()
        // 打开连接(初始化请求对象)
        request.open(method, url, true)
        // 设置响应数据类型 ==> 自动解析json文本为js对象/数组, 保存给response属性上
        request.responseType = 'json'
        // 绑定监视request的状态改变的监听
        request.onreadystatechange = function () {
          // 如果请求还没有完成, 直接结束
          if (request.readyState!==4) {
            return
          }
          const {status, statusText} = request
          // 如果成功了, 取出数据封装成成功的响应数据对象response, 调用resolve(response)
          if (status>=200 && status<300) { // 在[200, 300)
            const response = {
              // data: JSON.parse(request.response),
              data: request.response,
              status,
              statusText
            }
            resolve(response)
          } else {
             // 如果失败了, 封装失败相关信息成error对象, 调用reject(error)
             reject(new Error('request error status is ' + status))
          }
        }
        if (method==='GET' || method==='DELETE') {
          // 发送请求
          request.send()
        } else { // POST/PUT
          // 设置请求头
          request.setRequestHeader('Content-Type', 'application/json;charset=utf-8')
          // 发送请求
          request.send(JSON.stringify(data))
        }
      })
    }
```

####  2.7.3使用测试
```js
function testGet() {
      axios({
        url: 'http://localhost:3000/comments',
        // url: 'http://localhost:3000/comments2',
        params: {id: 3},
      }).then(response => {
        console.log('get success', response.data, response)
      }).catch(error => {
        alert(error.message)
      })
    }

    function testPost() {
      axios({
        url: 'http://localhost:3000/comments',
        // url: 'http://localhost:3000/comments2',
        method: 'POST',
        data: { body: 'aaaa', postId: 2 }
      }).then(response => {
        console.log('post success', response.data, response)
      }).catch(error => {
        alert(error.message)
      })
}

    function testPut() {
      axios({
        url: 'http://localhost:3000/comments/3',
        // url: 'http://localhost:3000/comments/39',
        method: 'put',
        data: {body: 'abcdefg', "postId": 2}
      }).then(response => {
        console.log('put success', response.data, response)
      }).catch(error => {
        alert(error.message)
      })
    }
    
    function testDelete() {
      axios({
        url: 'http://localhost:3000/comments/1',
        method: 'delete',
        params: {
          body: 'some comment'
        }
      }).then(response => {
        console.log('delete success', response.data, response)
      }).catch(error => {
        alert(error.message)
      })
    }
```

### 第3章：axios的理解和使用

#### 1.1axios是什么?

\1. 前端最流行的ajax请求库

\2. react/vue官方都推荐使用axios发ajax请求

\3. 文档: https://github.com/axios/axios

## **1.2.** ***\*axios特点\****

\1. 基于xhr + promise的异步ajax请求库

\2. 浏览器端/node端都可以使用

\3. 支持请求／响应拦截器

\4. 支持请求取消

\5. 请求/响应数据转换

\6. 批量发送多个请求

#### 1.3.axios常用语法

axios(config): 通用/最本质的发任意类型请求的方式

axios(url[, config]): 可以只指定url发get请求

axios.request(config): 等同于axios(config)

axios.get(url[, config]): 发get请求

axios.delete(url[, config]): 发delete请求

axios.post(url[, data, config]): 发post请求

axios.put(url[, data, config]): 发put请求

 

axios.defaults.xxx: 请求的默认全局配置

axios.interceptors.request.use(): 添加请求拦截器

axios.interceptors.response.use(): 添加响应拦截器

 

axios.create([config]): 创建一个新的axios(它没有下面的功能)

 

axios.Cancel(): 用于创建取消请求的错误对象

axios.CancelToken(): 用于创建取消请求的token对象

axios.isCancel(): 是否是一个取消请求的错误

axios.all(promises): 用于批量执行多个异步请求

axios.spread(): 用来指定接收所有成功数据的回调函数的方法

![img](Untitled%202.assets/wps1.png) 

#### 1.4难点语法的理解和使用

### **1.4.1.** ***\*axios.create(config)\** 

\1. 根据指定配置创建一个新的axios, 也就就每个新axios都有自己的配置

\2. 新axios只是没有取消请求和批量发请求的方法, 其它所有语法都是一致的

\3. 为什么要设计这个语法?

(1) 需求: 项目中有部分接口需要的配置与另一部分接口需要的配置不太一样, 如何处理

(2) 解决: 创建2个新axios, 每个都有自己特有的配置, 分别应用到不同要求的接口请求中

### ***\*拦截器函数/ajax请求/请求的回调函数的调用顺序\****

\1. 说明: 调用axios()并不是立即发送ajax请求, 而是需要经历一个较长的流程

\2. 流程: 请求拦截器2 => 请求拦截器1 => 发ajax请求 => 响应拦截器1 => 响应拦截器2 => 请求的回调

\3. 注意: 此流程是通过promise串连起来的, 请求拦截器传递的是config, 响应拦截器传递的是response

### 1.4.2.取消请求

\1. 基本流程

配置cancelToken对象

  缓存用于取消请求的cancel函数

  在后面特定时机调用cancel函数取消请求

  在错误回调中判断如果error是cancel, 做相应处理

\2. 实现功能

  点击按钮, 取消某个正在请求中的请求

在请求一个接口前, 取消前面一个未完成的请求