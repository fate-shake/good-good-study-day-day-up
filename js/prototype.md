# 原型和原型链
> 在 javaScript 中，每个对象都有一个指向它的原型（prototype）对象的内部链接。这个原型对象又有自己的原型，直到某个对象的原型为 null 为止（也就是不再有原型指向），组成这条链的最后一环。这种一级一级的链结构就称为原型链（prototype chain）。

#### 对象的创建
不是类

1、obj = new Object(); obj.name = 'name'

2、obj = {}

3、obj = new fun()

4、Object.create()

#### 查看对象原型
obj.\__proto__

obj.getPrototypeOf() --- 推荐用法

函数对象特有属性：fn.prototype

#### 操作原型
setPrototypeOf: 设置指定对象的原型到另一个对象或者null

hasOwnProperty(): 返回自身属性是否包含指定属性(该方法会忽略从原型上继承的属性)

defineProperty(): 在对象上直接定义或修改一个属性
