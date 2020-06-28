```js
function Promise(executor){
    this._status = 'pending'
    this._value = undefined
    this._callbacks = {}
    const resolve = value =>{
        if(this._status === 'pending'){
            this._status = 'resolved'
            this._value = value
            setTimeout(() =>{ this._callbacks.onResolve(value)})
        }
    }
    const reject = reason =>{
        if(this._status === 'pending'){
            this._status = 'rejected'
            this._value = reason
            setTimeout(() =>{ this._callbacks.onReject(reason)})
        }
    }
    try{executor(resolve,reject)}catch(e){reject(e)}
}
Promise.prototype.then = function (onResolve,onReject){
    onResolve = onResolve ? onResolve : value => value
    onReject = onReject ? onReject : reason =>{throw reason}
    switch (this._status) {
        case 'resolved':
            return new Promise((resolve,reject) =>{
                promise(onResolve,this._value,resolve,reject)  
            })
        case 'rejected':
            return new Promise((resolve,reject) =>{
                promise(onReject,this._value,resolve,reject) 
            })
        case 'pending':
            return new Promise((resolve,reject) =>{
                this._callbacks.onResolve = function(){
                    promise(onResolve,this._value,resolve,reject) 
                }
                this._callbacks.onReject = function(){
                    promise(onReject,this._value,resolve,reject)
                }
            })
    }  
}
function promise(onFn,value,resolve,reject){
    setTimeout(() =>{
        try {
            const res = onFn(value)
            res instanceof Promise ?  res.then(resolve,reject) : resolve(res) 
        } catch (e) {
            reject(e)
        }
    })
}
Promise.prototype.catch = function(onReject){
    return this.then(undefined,onReject)
}
```

