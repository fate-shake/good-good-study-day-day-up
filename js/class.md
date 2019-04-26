# 类与继承
### 类
JavaScript严格意义上是没有类的，知道es6定义了。。。

JavaScript类的实现是基于原型和原型链的；

es5中通过构造函数来实现类：
```js
function A () {
    this.name = 'A'
    this.say = function () {
        console.log('A')
    }
}// A 类
```

### 继承
JavaScript继承的方式有多种
#### 类继承
```js
function A () {
    this.name = 'A'
    this.say = function () {
        console.log('A')
    }
}
A.prototype.sayName = function () {
    console.log(this.name)
}
function B () {
    this.name = 'B'
}
B.prototype = new A()
```

#### 构造函数继承
```js
function A () {
    this.name = 'A'
    this.say = function () {
        console.log('A')
    }
}
A.prototype.sayName = function () {
    coonsole.log(this.name)
}
function B () {
    A.apply(this,arguments)
}
```

#### 组合继承
```js
function A () {
    this.name = 'A'
    this.say = function () {
        console.log('A')
    }
}
A.prototype.sayName = function () {
    coonsole.log(this.name)
}
// 关键下面这几句代码
function B () {
    // 构造函数继承
    A.apply(this,arguments)
}
// 类继承
B.prototype = new A()
```

#### 寄生组合继承
```js
function A () {
    this.name = 'A'
    this.say = function () {
        console.log('A')
    }
}
A.prototype.sayName = function () {
    coonsole.log(this.name)
}
// 关键下面这几句代码
function B () {
    // 构造函数继承
    A.apply(this,arguments)
}
B.prototype = Object.create(A.prototype)
B.prototype.contrustor = B
```

#### ES6 extends 继承
```js
class A {
    constructor () {
        this.name = 'A'
    }
    say () {
        console.log(this.name)
    }
}
class B extends A {
    constructor () {
        super()
        this.name = 'B'
    }
}
// 子类的初始化函数constructor中必须调用super来获取父类的this，否则会报错
```
> 关于各个继承方式的优劣放在未来补充，此次只做大致了解类与继承

> 2019/4/26