# 第1章：准备

#### 1.1. 区别实例对象与函数对象

1）实例对象: new 函数产生的对象, 称为实例对象, 简称为对象

2）函数对象: 将函数作为对象使用时, 简称为函数对象

~~~js
function Fn() { // Fn是函数
  
}
const fn = new Fn() // Fn是构造函数  new返回的是实例对象
console.log(Fn.prototype) // Fn是函数对象
Fn.call({}) // Fn是函数对象

$('#test') // $是函数
$.ajax() // $是函数对象 
/* 
总结
  1. 点的左边是对象(可能是实例对象也可能是函数对象)
  2. ()的左边是函数
*/
~~~

#### 1.1.二种类型的回调函数

1.2.1.==同步回调== 
1）理解: 立即执行, 完全执行完了才结束, 不会放入回调队列中
2）例子: 数组遍历相关的回调函数 / Promise的excutor函数
1.2.2.==异步回调==
1）理解: 不会立即执行, 会放入回调队列中将来执行
2）例子: 定时器回调 / ajax回调 / Promise的成功|失败的回调

```
/ 1. 同步回调函数
const arr = [1, 2, 3]
arr.forEach(item => {// 同步执行的回调函数, forEach()内部在执行完所有回调函数后才结束, 不会放入回调队列中
  console.log('forEach callback()', item)
})
console.log('forEach()之后')

// 2. 异步回调函数
setTimeout(() => { // 异步执行的回调函数, setTimeout()在回调函数执行前就结束了, 回调会放入回调队列中在同步代码执行完后才会执行
  console.log('setTimeout callback()')
}, 0)
console.log('setTimeout()之后')
```
#### 1.3.JS的error处理
**1.3.1.错误的类型**

1）Error: 所有错误的父类型
2）ReferenceError: 引用的变量不存在
3）TypeError: 数据类型不正确的错误
4）RangeError: 数据值不在其所允许的范围内
5）SyntaxError: 语法错误

**1.3.2.错误处理**

1）捕获错误: try ... catch
2）抛出错误: throw error

**1.3.3.error对象的结构**

1）==message==属性: 错误相关信息
2）==stack==属性: 函数调用栈记录信息

```js
//1. 常见内置错误
*/
// ReferenceError: 引用的变量不存在
// console.log(a) // ReferenceError: a is not defined

// TypeError: 数据类型不正确的错误
var b = null
// console.log(b.xxx) // TypeError: Cannot read property 'xxx' of null
b = 3
// console.log(b.xxx())  // TypeError: b.xxx is not a function
// RangeError: 数据值不在其所允许的范围内
function fn1() {
  fn1()
}
// fn1() // RangeError: Maximum call stack size exceeded
// SyntaxError: 语法错误
// const c = """"  // SyntaxError: Unexpected string
/* 
2. 错误处理
*/
// 2.1 捕获错误
try {
  var d = 3
  d()
} catch (error) {
  console.log(error.message)
  console.log(error.stack)
}
console.log('捕获错误后还可以继续执行')
// 2.2 抛出错误
function doThing() {
  const time = Date.now()
  if (time %2 === 1) {
    console.log('当前是奇数, 可以执行业务逻辑处理')
  } else {
    throw new Error('当前时间是偶数, 无法处理业务逻辑')
  }
}
try {
  doThing()
} catch (error) { // 捕获错误, 做相应的界面提示
  alert(error.message)
} 
```
# 第2章：Promise的理解和使用
### 2.1. Promise是什么?*重点
**2.1.1. 理解**

1. 抽象表达: 
    ==1）Promise是一门新的技术(ES6规范)
    2）Promise是JS中进行异步编程的新解决方案
备注：旧方案是单纯使用回调函数==
2. 具体表达:
    ==1）从语法上来说: Promise是一个构造函数
    2）从功能上来说: promise对象用来封装一个异步操作并可以获取其成功/失败的结果值==

**2.1.2. promise的状态改变**

1. pending变为**resolved**
2. pending变为**rejected**
>说明: 只有这2种, 且一个promise对象只能改变一次
      无论变为成功还是失败, 都会有一个结果数据
      成功的结果数据一般称为value, 失败的结果数据一般称为reason

### promise的基本流程

![1592463126261](C:\Users\leilinghui\Desktop\笔记\node\promise.assets\1592463126261.png)

**2.1.4. promise的基本使用**
1） 使用1: 基本编码流程

~~~js
<script>
  // 1) 创建promise对象(pending状态), 指定执行器函数
  const p = new Promise((resolve, reject) => {
    // 2) 在执行器函数中启动异步任务
    setTimeout(() => {
      const time = Date.now()
      // 3) 根据结果做不同处理
      // 3.1) 如果成功了, 调用resolve(), 指定成功的value, 变为resolved状态
      if (time%2===1) {
        resolve('成功的值 '+ time)
      } else { // 3.2) 如果失败了, 调用reject(), 指定失败的reason, 变为rejected状态
        reject('失败的值' + time)
      }
    }, 2000)
  })

  // 4) 能promise指定成功或失败的回调函数来获取成功的vlaue或失败的reason
  p.then(
    value => { // 成功的回调函数onResolved, 得到成功的vlaue
      console.log('成功的value: ', value)
    },
    reason => { // 失败的回调函数onRejected, 得到失败的reason
      console.log('失败的reason: ', reason)
    }
  )
</script>

2)使用2: 使用promise封装基于定时器的异步
<script>
  function doDelay(time) {
    // 1. 创建promise对象
    return new Promise((resolve, reject) => {
      // 2. 启动异步任务
      console.log('启动异步任务')
      setTimeout(() => {
        console.log('延迟任务开始执行...')
        const time = Date.now() // 假设: 时间为奇数代表成功, 为偶数代表失败
        if (time %2=== 1) { // 成功了
          // 3. 1. 如果成功了, 调用resolve()并传入成功的value
          resolve('成功的数据 ' + time)
        } else { // 失败了
          // 3.2. 如果失败了, 调用reject()并传入失败的reason
          reject('失败的数据 ' + time)
        }
      }, time)
    })
  }
const promise = doDelay(2000)
  promise.then(
    value => {
      console.log('成功的value: ', value)
    },
    reason => {
      console.log('失败的reason: ', reason)
    },
  )
</script>
~~~

3）使用3: 使用promise封装ajax异步请求
~~~js
<script>
  /* 
  可复用的发ajax请求的函数: xhr + promise
  */
  function promiseAjax(url) {
    return new Promise((resolve, reject) => {
      const xhr = new XMLHttpRequest()
      xhr.onreadystatechange = () => {
        if (xhr.readyState!==4) return

        const {status, response} = xhr
        // 请求成功, 调用resolve(value)
        //2开头的都是成功 3 重定向 4客户端错误 5 服务器错误
        if (status>=200 && status<300) {
          resolve(JSON.parse(response))
        } else {  // 请求失败, 调用reject(reason)
          reject(new Error('请求失败: status: ' + status))
        }
      }
      xhr.open("GET", url)
      xhr.send()
    })
  }
  promiseAjax('https://api.apiopen.top2/getJoke?page=1&count=2&type=video')
    .then(
      data => {
        console.log('显示成功数据', data)
      },
      error => {
        alert(error.message)
      }
    )
</script>
~~~
### 2.2. 为什么要用Promise?
**2.2.1. 指定回调函数的方式更加灵活**
1. 旧的: 必须在启动异步任务前指定
2. promise: 启动异步任务 => 返回promie对象 => 给promise对象绑定回调函数(甚至可以在异步任务结束后指定/多个)
1. 什么是回调地狱? 
	回调函数嵌套调用, 外部回调函数异步执行的结果是嵌套的回调执行的条件
2. 回调地狱的缺点?  
    不便于阅读
    不便于异常处理
3. 解决方案?
	promise链式调用
4. 终极解决方案?
	async/await

**2.2.2. 支持链式调用, 可以解决回调地狱问题**

```js
<script>
  /* 
  1. 指定回调函数的方式更加灵活: 
    旧的: 必须在启动异步任务前指定
    promise: 启动异步任务 => 返回promie对象 => 给promise对象绑定回调函数(甚至可以在异步任务结束后指定)

  2. 支持链式调用, 可以解决回调地狱问题
    什么是回调地狱? 回调函数嵌套调用, 外部回调函数异步执行的结果是嵌套的回调函数执行的条件
    回调地狱的缺点?  不便于阅读 / 不便于异常处理
    解决方案? promise链式调用
    终极解决方案? async/await
  */

  // 成功的回调函数
  function successCallback(result) {
    console.log("声音文件创建成功: " + result);
  }
  // 失败的回调函数
  function failureCallback(error) {
    console.log("声音文件创建失败: " + error);
  }

  /* 1.1 使用纯回调函数 */
  createAudioFileAsync(audioSettings, successCallback, failureCallback)
  
/* 1.2. 使用Promise */
  const promise = createAudioFileAsync(audioSettings); // 2
  setTimeout(() => {
    promise.then(successCallback, failureCallback);
  }, 3000);
  
  /* 
  2.1. 回调地狱
  */
  doSomething(function(result) {
    doSomethingElse(result, function(newResult) {
      doThirdThing(newResult, function(finalResult) {
        console.log('Got the final result: ' + finalResult)
      }, failureCallback)
    }, failureCallback)
  }, failureCallback)

  /* 
  2.2. 使用promise的链式调用解决回调地狱
  */
  doSomething().then(function(result) {
    return doSomethingElse(result)
  })
  .then(function(newResult) {
    return doThirdThing(newResult)
  })
  .then(function(finalResult) {
    console.log('Got the final result: ' + finalResult)
  })
  .catch(failureCallback)

  /* 
  2.3. async/await: 回调地狱的终极解决方案
  */
  async function request() {
    try {
      const result = await doSomething()
      const newResult = await doSomethingElse(result)
      const finalResult = await doThirdThing(newResult)
      console.log('Got the final result: ' + finalResult)
    } catch (error) {
      failureCallback(error)
    }
  }
</script>
```


### 2.3. 如何使用Promise?

---

**2.3.1. API**
1.	Promise构造函数: Promise (excutor) {}
    (1)executor函数: ==执行器函数==  (resolve, reject) => {} 
    (2)resolve函数: 内部定义成功时我们调用的函数 value => {}
    (3)reject函数: 内部定义失败时我们调用的函数 reason => {}
说明: executor会在Promise内部立即同步调用,异步操作在执行器中执行

2. Promise.prototype.==then==方法: (onResolved, onRejected) => {}
    (1)onResolved函数: ==成功==的回调函数  (value) => {}
    (2)onRejected函数: ==失败==的回调函数 (reason) => {}
说明: 指定用于得到成功value的成功回调和用于得到失败reason的失败回调

3. 返回一个新的promise对象

4. Promise.prototype.==catch==方法: (onRejected) => {}
    (1)onRejected函数: ==失败==的回调函数 (reason) => {}
    说明: then()的语法糖, 相当于: then(undefined, onRejected)

5. Promise.==resolve==方法: (value) => {}
    (1)value: 成功的数据或promise对象
    说明: 返回一个成功/失败的promise对象

    ![1592537394364](C:\Users\leilinghui\Desktop\笔记\node\promise.assets\1592537394364.png)

6. Promise.==reject==方法: (reason) => {}
    (1)reason: 失败的原因
    说明: 返回一个失败的promise对象

7. Promise.all方法: (promises) => {}//例如 promise.all([one,two]))
  (1)promises: 包含n个promise的数组
  说明: 返回一个新的promise, 只有所有的promise都成功才成功, 只要有一个失败了就直接失败

8. Promise.race方法: (promises) => {}
  (1)promises: 包含n个promise的数组
  说明: 返回一个新的promise, 第一个完成的promise的结果状态就是最终的结果状态

  ==谁先完成谁决定rece的方法的返回结果==
```js
<script>

  /* 
    1. Promise构造函数: Promise (excutor) {}
        excutor函数: 同步执行  (resolve, reject) => {}
        resolve函数: 内部定义成功时我们调用的函数 value => {}
        reject函数: 内部定义失败时我们调用的函数 reason => {}
        说明: excutor会在Promise内部立即同步回调,异步操作在执行器中执行
    2. Promise.prototype.then方法: (onResolved, onRejected) => {}
        onResolved函数: 成功的回调函数  (value) => {}
        onRejected函数: 失败的回调函数 (reason) => {}
        说明: 指定用于得到成功value的成功回调和用于得到失败reason的失败回调
              返回一个新的promise对象
    3. Promise.prototype.catch方法: (onRejected) => {}
        onRejected函数: 失败的回调函数 (reason) => {}
        说明: then()的语法糖, 相当于: then(undefined, onRejected)
    4. Promise.resolve方法: (value) => {}
        value: 成功的数据或promise对象
        说明: 返回一个成功/失败的promise对象
    5. Promise.reject方法: (reason) => {}
        reason: 失败的原因
        说明: 返回一个失败的promise对象
    6. Promise.all方法: (promises) => {}
        promises: 包含n个promise的数组
        说明: 返回一个新的promise, 只有所有的promise都成功才成功, 只要有一个失败了就直接失败
    7. Promise.race方法: (promises) => {}
        promises: 包含n个promise的数组
        说明: 返回一个新的promise, 第一个完成的promise的结果状态就是最终的结果状态
  */
  
  /* 
  new Promise((resolve, reject) => {
    if (Date.now()%2===0) {
      resolve(1)
    } else {
      reject(2)
    }
  }).then(value => {
    console.log('onResolved1()', value)
  }).catch(reason => {
    console.log('onRejected1()', reason)
  })
  */
  
  const p1 = Promise.resolve(1)
  const p2 = Promise.resolve(Promise.resolve(3))
  const p3 = Promise.resolve(Promise.reject(5))
  const p4 = Promise.reject(7)
  const p5 = new Promise((resolve, reject) => {
    setTimeout(() => {
      if (Date.now()%2===0) {
        resolve(1)
      } else {
        reject(2)
      }
    }, 100);
  })

  const pAll = Promise.all([p1, p2, p5])
  pAll.then(
    values => {console.log('all成功了', values)},
    reason => {console.log('all失败了', reason)}
  )

  // const pRace = Promise.race([p5, p4, p1])
  const pRace = Promise.race([p5, p1, p4])
  pRace.then(
    value => {console.log('race成功了', value)},
    reason => {console.log('race失败了', reason)}
  )
</script>
```
### 2.3.2. promise的几个关键问题
1. 如何改变promise的状态?
    (1)resolve(value): 如果当前是pending就会变为resolved
    (2)reject(reason): 如果当前是pending就会变为rejected
    (3)抛出异常: 如果当前是pending就会变为rejected
    
2. 一个promise指定多个成功/失败回调函数, 都会调用吗?
	当promise改变为对应状态时都会调用

3. 改变promise状态和指定回调函数谁先谁后?
    (1)都有可能, 正常情况下是先指定回调再改变状态, 但也可以先改状态再指定回调
    (2)如何先改状态再指定回调?
        1)在执行器中直接调用resolve()/reject()
        2)延迟更长时间才调用then()
	(3)什么时候才能得到数据?
        1)如果先指定的回调, 那当状态发生改变时, 回调函数就会调用, 得到数据
        2)如果先改变的状态, 那当指定回调时, 回调函数就会调用, 得到数据

4. promise.then()返回的新promise的结果状态由什么决定?
    (1)简单表达: 由then()指定的回调函数执行的结果决定
    (2)详细表达:
        ①如果抛出异常, 新promise变为rejected, reason为抛出的异常
        ②如果返回的是非promise的任意值, 新promise变为resolved, value为返回的值
        ③如果返回的是另一个新promise, 此promise的结果就会成为新promise的结果 
5. promise如何串连多个操作任务?
    (1)promise的then()返回一个新的promise, 可以开成then()的链式调用
    (2)通过then的链式调用串连多个同步/异步任务
6.promise异常传透?
    (1)当使用promise的then链式调用时, 可以在最后指定失败的回调, 
    (2)前面任何操作出了异常, 都会传到最后失败的回调中处理
7.中断promise链?
    (1)当使用promise的then链式调用时, 在中间中断, 不再调用后面的回调函数
    (2)办法: 在回调函数中返回一个pendding状态的promise对象

---

# 第3章：自定义(手写)Promise
### 3.1. 定义整体结构
```js
(function (window) {
  /*
  Promise构造函数
  excutor: 内部同步执行的函数  (resolve, reject) => {}
   */
  function Promise(excutor) {
  }
  /*
  为promise指定成功/失败的回调函数
  函数的返回值是一个新的promise对象
   */
  Promise.prototype.then = function (onResolved, onRejected) {
  }
  /*
  为promise指定失败的回调函数
  是then(null, onRejected)的语法糖
   */
  Promise.prototype.catch = function (onRejected) {
  }

  /*
  返回一个指定了成功value的promise对象
   */
  Promise.resolve = function (value) {
  }

  /*
  返回一个指定了失败reason的promise对象
   */
  Promise.reject = function (reason) {
  }

  /*
  返回一个promise, 只有promises中所有promise都成功时, 才最终成功, 只要有一个失败就直接失败
   */
  Promise.all = function (promises) {
  }

  /*
  返回一个 promise， 一旦某个promise解决或拒绝， 返回的 promise就会解决或拒绝。
  */
  Promise.race = function (promises) {
    
  }

  // 暴露构造函数
  window.Promise = Promise
})(window)
```
### 3.2Promise构造函数的实现
``` js
/*
Promise构造函数
excutor: 内部同步执行的函数  (resolve, reject) => {}
  */
function Promise(excutor) {

  const self = this
  self.status = 'pending' // 状态值, 初始状态为pending, 成功了变为resolved, 失败了变为rejected
  self.data = undefined // 用来保存成功value或失败reason的属性
  self.callbacks = [] // 用来保存所有待调用的包含onResolved和onRejected回调函数的对象的数组
  /*
  异步处理成功后应该调用的函数
  value: 将交给onResolve()的成功数据
    */
  function resolve(value) {
    if(self.status!=='pending') { // 如果当前不是pending, 直接结束
      return
    }
    // 立即更新状态, 保存数据
    self.status = 'resolved'
    self.data = value
    // 异步调用所有待处理的onResolved成功回调函数
    if (self.callbacks.length>0) {
      setTimeout(() => {
        self.callbacks.forEach(obj => {
          obj.onResolved(value)
        })
      })
    }
    
  }

  /*
  异步处理失败后应该调用的函数
  reason: 将交给onRejected()的失败数据
    */
  function reject(reason) {

    if(self.status!=='pending') { // 如果当前不是pending, 直接结束
      return
}

    // 立即更新状态, 保存数据
    self.status = 'rejected'
    self.data = reason
    // 异步调用所有待处理的onRejected回调函数
    setTimeout(() => {
      self.callbacks.forEach(obj => {
        obj.onRejected(reason)
      })
    })
  }

  try {
    // 立即同步调用excutor()处理
    excutor(resolve, reject)
  } catch (error) { // 如果出了异常, 直接失败
    reject(error)
  }
}
```
### 3.3. promise.then()/catch()的实现
``` js
/*
为promise指定成功/失败的回调函数
函数的返回值是一个新的promise对象
*/
Promise.prototype.then = function (onResolved, onRejected) {
  const self = this

  // 如果onResolved/onRejected不是函数, 可它指定一个默认的函数
  onResolved = typeof onResolved==='function' ? onResolved : value => value  // 指定返回的promise为一个成功状态, 结果值为 value
  onRejected = typeof onRejected === 'function' ? onRejected : reason => {throw reason} // 指定返回的promise为一个失败状态, 结果值为reason
  // 返回一个新的promise对象
  return new Promise((resolve, reject) => {
    /* 
    专门抽取的用来处理promise成功/失败结果的函数
    callback: 成功/失败的回调函数
    */
    function handle(callback) {
      // 1. 抛出异常  ===> 返回的promise变为rejected
      try {
        const x = callback(self.data)
        // 2. 返回一个新的promise ===> 得到新的promise的结果值作为返回的promise的结果值
        if (x instanceof Promise) {
          x.then(resolve, reject) // 一旦x成功了, resolve(value), 一旦x失败了: reject(reason)
        } else {
          // 3. 返回一个一般值(undefined) ===> 将这个值作为返回的promise的成功值
          resolve(x)
        }
      } catch (error) {
        reject(error)
      }
    }
    if (self.status === 'resolved') { // 当前promise已经成功了
      setTimeout(() => {
        handle(onResolved)
      })
    } else if (self.status === 'rejected') { // 当前promise已经失败了
      setTimeout(() => {
        handle(onRejected)
      })
    } else { // 当前promise还未确定 pending
      // 将onResolved和onRejected保存起来
      self.callbacks.push({
        onResolved(value) {
          handle(onResolved)
        },
        onRejected(reason) {
          handle(onRejected)
        }
      })
    }
  })
}
/*
为promise指定失败的回调函数
是then(null, onRejected)的语法糖
  */
Promise.prototype.catch = function (onRejected) {
  return this.then(null, onRejected)
```

### 3.4. Promise.resolve()/reject()的实现
``` js
*
返回一个指定了成功value的promise对象
value: 一般数据或promise
  */
Promise.resolve = function (value) {
  return new Promise((resolve, reject) => {
    if (value instanceof Promise) {
      value.then(resolve, reject)
    } else {
      resolve(value)
    }
  })
}

/*
返回一个指定了失败reason的promise对象
reason: 一般数据/error
  */
Promise.reject = function (reason) {
  return new Promise((resolve, reject) => {
    reject(reason)
  })
}
```
###  3.5. Promise.all/race()的实现
``` js
/*
返回一个新的promise对象, 只有promises中所有promise都产生成功value时, 才最终成功, 只要有一个失败就直接失败
*/
Promise.all = function (promises) {
  // 返回一个新的promise
  return new Promise((resolve, reject) => {
    // 已成功的数量
    let resolvedCount = 0
    // 待处理的promises数组的长度
    const promisesLength = promises.length
    // 准备一个保存成功值的数组
    const values = new Array(promisesLength)
    // 遍历每个待处理的promise
    for (let i = 0; i < promisesLength; i++) {
      // promises中元素可能不是一个数组, 需要用resolve包装一下
      Promise.resolve(promises[i]).then(
        value => {
          // 成功当前promise成功的值到对应的下标
          values[i] = value
          // 成功的数量加1
          resolvedCount++
          // 一旦全部成功
          if(resolvedCount===promisesLength) {
            // 将所有成功值的数组作为返回promise对象的成功结果值
            resolve(values)
          }
        },
        reason => {
          // 一旦有一个promise产生了失败结果值, 将其作为返回promise对象的失败结果值
          reject(reason)
        }
      )
    }
  })
}

/*
返回一个 promise，一旦某个promise解决或拒绝， 返回的 promise就会解决或拒绝。
*/
Promise.race = function (promises) {
  // 返回新的promise对象
  return new Promise((resolve, reject) => {
    // 遍历所有promise
    for (var i = 0; i < promises.length; i++) {
      Promise.resolve(promises[i]).then(
        (value) => { // 只要有一个成功了, 返回的promise就成功了
          resolve(value)
        },
        (reason) => { // 只要有一个失败了, 返回的结果就失败了
          reject(reason)
        }
      )
    }
  })
}
```
### 3.6. Promise.resolveDelay()/rejectDelay()的实现
``` js
* 
  返回一个延迟指定时间才确定结果的promise对象
*/
Promise.resolveDelay = function (value, time) {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      if (value instanceof Promise) { // 如果value是一个promise, 取这个promise的结果值作为返回的promise的结果值
        value.then(resolve, reject) // 如果value成功, 调用resolve(val), 如果value失败了, 调用reject(reason)
      } else {
        resolve(value)
      }
    }, time);
  })
}

/*
返回一个延迟指定时间才失败的Promise对象。
*/
Promise.rejectDelay = function (reason, time) {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      reject(reason)
    }, time)
  })
}
```
3.7. ES5 function完整版本

![img](C:\Users\leilinghui\Desktop\笔记\node\promise.assets\wps5.png)

3.8. ES6 class完整版

![img](C:\Users\leilinghui\Desktop\笔记\node\promise.assets\wps6.png)

# 第4章：async与await
### 4.1. mdn文档
https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Statements/async_function
https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Operators/await
### 4.2. async 函数
1. 函数的返回值为promise对象
2. promise对象的结果由async函数执行的返回值决定
### 4.3. await 表达式
1. await右侧的表达式一般为promise对象, 但也可以是其它的值
2. 如果表达式是promise对象, await返回的是promise成功的值
3. 如果表达式是其它值, 直接将此值作为await的返回值
### 4.4. 注意
1. await必须写在async函数中, 但async函数中可以没有await
2. 如果await的promise失败了, 就会抛出异常, 需要通过try...catch捕获处理
``` js
<script>
  function fn1() {
    return Promise.resolve(1)
  }

  function fn2() {
    return 2
  }

  function fn3() {
    return Promise.reject(3)
    // return fn3.test() // 程序运行会抛出异常
  }

  function fn4() {
    return fn3.test() // 程序运行会抛出异常
  }

  // 没有使用await的async函数
  async function fn5() {
    return 4
  }

  async function fn() {
    // await右侧是一个成功的promise
    const result = await fn1()
    // await右侧是一个非promise的数据
    // const result = await fn2()
    // await右侧是一个失败的promise
    // const result = await fn3()
    // await右侧抛出异常
    // const result = await fn4()
    console.log('result: ', result)
    return result+10
  }

  async function test() {
    try {
      const result2 = await fn()
      console.log('result2', result2)
    } catch (error) {
      console.log('error', error)
    }
    const result3 = await fn4()
    console.log('result4', result3)
  }
  // test()
</script>
```

# 第5章：JS异步之宏队列与微队列
### 5.1. 原理图

![1592464813126](C:\Users\leilinghui\Desktop\笔记\node\promise.assets\1592464813126.png)
### 5.2. 说明
1. JS中用来存储待执行回调函数的队列包含2个不同特定的列队
2. 宏列队: 用来保存待执行的宏任务(回调), 比如: 定时器回调/DOM事件回调/ajax回调
3. 微列队: 用来保存待执行的微任务(回调), 比如: promise的回调/MutationObserver的回调
4. JS执行时会区别这2个队列
    (1)JS引擎首先必须先执行所有的初始化同步任务代码
    (2)每次准备取出第一个宏任务执行前, 都要将所有的微任务一个一个取出来执行
# 第6章：promise相关面试题
### 6.1. 面试题1
``` js
script type="text/javascript">
  setTimeout(()=>{
    console.log(1)
  },0)
  Promise.resolve().then(()=>{
    console.log(2)
  })
  Promise.resolve().then(()=>{
    console.log(4)
  })
  console.log(3)
</script>
```
### 6.2. 面试题2
``` js
<script type="text/javascript">
  setTimeout(() => {
    console.log(1)
  }, 0)
  new Promise((resolve) => {
    console.log(2)
    resolve()
  }).then(() => {
    console.log(3)
  }).then(() => {
    console.log(4)
  })
  console.log(5)

</script>
```
### 6.3. 面试题3
``` js
<script type="text/javascript">
  const first = () => (new Promise((resolve, reject) => {
    console.log(3)
    let p = new Promise((resolve, reject) => {
      console.log(7)
      setTimeout(() => {
        console.log(5)
        resolve(6)
      }, 0)
      resolve(1)
    })
    resolve(2)
    p.then((arg) => {
      console.log(arg)
    })

  }))

  first().then((arg) => {
    console.log(arg)
  })
  console.log(4)
</script>
```
### 6.4. 面试题4
``` js
script type="text/javascript">
  setTimeout(() => {
    console.log("0")
  }, 0)
  new Promise((resolve,reject)=>{
    console.log("1")
    resolve()
  }).then(()=>{        
    console.log("2")
    new Promise((resolve,reject)=>{
      console.log("3")
      resolve()
    }).then(()=>{      
      console.log("4")
    }).then(()=>{       
      console.log("5")
    })
  }).then(()=>{  
    console.log("6")
  })

  new Promise((resolve,reject)=>{
    console.log("7")
    resolve()
  }).then(()=>{         
    console.log("8")
  })
</script>
```
