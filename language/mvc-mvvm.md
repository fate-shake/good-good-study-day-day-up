# 设计模式(MVC、MVVM)
相同的部分就是：M、V

不同的部分就是：C、VM
### MVC
#### M-model
model层用于封装和应用程序的业务逻辑相关的数据和处理方法

#### V-view
view层用于向用户展示数据

#### 实现
对于MVC模式来说，当model层数据发生变化后，model变会通知相关联的视图即view进行更新；
model层和view层使用了观察者模式；
view和controller之间使用了策略模式；
controller是model层 和view层的纽带，MVC将响应机制封装在controller中，当用户与应用进行交互时，controller中的事件便开始工作了；
view变化--->触发controller中的事件处理--->改变model
model变化--->通知view更新

### MVVM
#### M-model
model数据层，只关心数据本身；

#### V-view
通过模板语法声明式的将数据渲染进DOM，当viewmodel对model进行更新时，会通过数据绑定更新到view

#### VM-ViewModel
view和model的数据同步交给了viewmodel的数据绑定进行处理，当model变化时，viewmodel会自动更新；viewmodel变化时，model也会更新；


## 梳理一下
### MVC
model变化--->通知view--->view更新

view变化--->触发controller中的事件--->model更新

### MVVM
通过模板将数据与视图绑定
当model变化时，viewmodel自动更新，因为数据原型与模板绑定，视图就更新了；
当view变化时，同样因数据原型与模板绑定，viewmodel更新后自动更新model


> 2019/4/25

