# 数据类型、类型判断
#### 数据类型
基础数据类型：String、Number、Boolean、null、undefined

复杂数据类型(？引用数据类型)：Object

其中object又包含：Array、Date、Error、RegExp、Function等

##### 关于内存空间
分为堆内存和栈内存

栈：主要用于存放基础数据类型，大小确定，系统自动分配内存空间，自动释放

堆：主要用于存放引用数据类型，大小不定，系统动态分配空间并不会自动释放


##### 关于数据拷贝（传值与传址）
当数据存放在栈内存中时，访问数据是直接对数据访问；当对数据拷贝时，拷贝的时数据本身值的拷贝，拷贝的对象与被拷贝对象就不存在关系了；

当数据存放在堆内存中时，JavaScript不允许直接访问堆内存中的位置，所以必须先从栈内存中获取数据的地址引用，然后再从堆内存中访问数据；当对数据进行拷贝时，拷贝的只是栈中的数据地址引用，然后再从堆中读取值；实际最终拷贝的对象引用地址没有发生改变；

##### 深拷贝
```js
// 粗暴方法，不考虑function
JSON.parse(JSON.stringity(obj))
```
```js
// 判断{}||[]
function getType (obj) {
    // [object Object] || [object Array]
    return Object.prototype.toString.call(obj).slice(8,-1)
}
function deepClone (target) {
    let result
    if (getType(target) === 'Object') {
        result = {}
    } else if (getType(target) === 'Array') {
        result = []
    } else {
        // 不是引用类型
        return target
    }
    for (let key in target) {
        if (getType(target) === 'Object' || getType(target) === 'Array') {
            result[key] = deepClone(target[key])
        } else {
            result[key] = target[key]
        }
    }
    return result
}
```

#### 类型判断
常用方法有typeof、Object.prototype.toString

##### typeof
对于基础数据类型，typeof基本能返回数据类型的小写值(null 返回object)

对于引用类型，typeof基本都返回objec(function 返回 function)

由此可见，typeof 不能精确返回数据的详细类型

##### Object.prototype.toString
Object.prototype.toString 返回的格式是：[object 类型]

 对于基础数据类型和引用类型，Object.prototype.toString都能准确的返回数据类型，因此最常用与判断数据类型；


> 2019/4/25 第一天
