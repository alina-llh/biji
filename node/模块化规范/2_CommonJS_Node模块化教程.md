## CommonJS服务端模块化教程(Node.js模块化教程)
### 规范
		说明
			http://wiki.commonjs.org/wiki/Modules/1.1
			每个文件都可当作一个模块
			在服务器端: 模块的加载是运行时同步加载的
			在浏览器端: 模块需要提前编译打包处理
		基本语法
			暴露模块
				module.exports = value
				exports.xxx = value
			引入模块
				require(xxx)
					第三方模块:xxx为模块名
					自定义模块: xxx为模块文件路径
### 实现
​	服务器端实现
​        Node.js
​        http://nodejs.cn/
​	浏览器端实现
​        Browserify
​        http://browserify.org/
​        也称为CommonJS的浏览器端的打包工具
​	区别Node与Browserify
​        Node.js运行时动态加载模块(同步)
​        Browserify是在转译(编译)时就会加载打包(合并)require的模块

### 1. 安装Node.js

### 2. 创建项目结构

  ```
  |-modules
    |-module1.js
    |-module2.js
    |-module3.js
  |-main.js
  |-package.json
  ```
### 3. 模块化编码：

  * module1.js
    ```
    module.exports = {
      data:'module1',
      foo(){
        console.log('foo()------',this.data);
      },
      bar(){
        console.log('bar()------',this.data);
      }
    }
    ```
  * module2.js
    ```
    module.exports = function () {
      console.log('module2');
    }
    ```
  * module3.js
    ```
    exports.foo = function () {
      console.log('foo()  module3');
    }
    
    exports.bar = function () {
      console.log('bar()  module3');
    }
    ```
  * 下载第三方模块uniq：，输入命令：```npm install uniq```

  * main.js 
    ```
    let module1 = require('./modules/module1')
    let module2 = require('./modules/module2')
    let module3 = require('./modules/module3')
    let a = require('uniq')
    
    module1.foo()
    module1.bar()
    module2()
    module3.foo()
    module3.bar()
    
    let arr = [1,11,2,2,2,5,5,5,3,4,6,6,9,7,8]
    console.log(a(arr));
      
    ```
###4. 在node环境下运行app.js的两种方法(任选其一)：
  * 第一种方法：用命令启动: ```node main.js```
  * 第二种方法：用工具启动: 右键 --> Run 'xxxxx.js'

