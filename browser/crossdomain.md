# 跨域
### 同源策略
浏览器的一种安全保护机制，不同源的客户端脚本在没有授权的情况下不能读取对方资源；

同源包括：协议相同、域名相同、端口相同

有一项不同则会发生跨域问题

### 跨域解决方案
#### jsonp
实现原理是通过script标签不受同源策略限制，通过在标签后添加回调函数来实现跨域

#### cors 跨域资源共享
当前最主流的跨域解决方案，在服务端设置Access-Control-Allow-Orgin字段

#### nginx代理


#### PostMessage
H5新api，主要用于两个窗口间通信，监听message事件和postmessage发送信息

#### webSocket
H5新增api，全双工通信，允许跨域通信

#### document.domain + iframe
#### window.name + iframe
#### location.href + iframe


> 2019/5/6