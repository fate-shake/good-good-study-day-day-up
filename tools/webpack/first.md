# webpack 入门1
主要参数了解：
+ entry：字符串、数组或者对象
    + 字符串：定义入口文件
    + 数组：一个参数定义入口文件，另一个用来配置静态资源服务器
    + 对象：不同的入口文件
+ output：对象，构建完成的文件输入，包含path和filename
+ module：对象，rules，各种loader的使用
+ resolve：extensitions，用于补全后缀
+ plugins：加载各种插件

> 2019/5/9