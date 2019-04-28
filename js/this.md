# this
> 在ES5中，this是谁调用就指向谁

在非严格模式中，全局对象window存在，若是全局调用，this指向window对象；
在严格模式中，window对象不存在，不能使用全局调用；

### 改变this指向
+ let _this = this
+ apply、call、bind
+ es6 箭头函数

#### apply、call、bind 区别
apply: 提供两个参数，第一个是指定this的值，第二个是需要传入的参数的<b>数组</b>

call: 第一个参数是指定this的值，之后的参数是需要传入参数<b>列表</b>

bind: bind是创建了一个新的函数，需要手动调用；传入参数方式与call相同

##### 手动实现bind
关键：this、arguments
```js
Function.prototype.myBind = function (obj) {
    // 获取myBind传参
    let arg = Array.prototype.slice.call(obj,1)
    let content = this
    let bind = function () {
        // 合并参数 myBind+bind
        arg = arg.concat(Array.prototype.slice.call(arguments))
        return content.apply(obj,arg)
    }
    let func = function () {}
    func.prototype = content.prototype
    bind.prototype = new func()
    return bind
}
```

> 2019/4/28