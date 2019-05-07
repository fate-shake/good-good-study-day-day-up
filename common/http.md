# HTTP、HTTPS
## HTTP 超文本传输协议

请求报文：方法，协议，URL，以及可选头部信息和请求内容

头部信息：host、connection、content-type、content-length

HTTP协议是不保存状态的，所以需要cookie信息来验证请求；

post与get请求的区别

1、get请求能够缓存，post不可以

2、post请求信息放在request body 里面，get请求放在URL上面

3、受限于浏览器，post可以传更多的请求数据，get不可以

4、post能够传更多的数据类型，get不可以

### 常见HTTP状态码
+ 200：请求被服务器正确处理
+ 301：永久重定向
+ 302：临时重定向
+ 304：允许访问资源，但并未返回，用于缓存
+ 403：请求方法不允许
+ 404：找不到被访问的资源
+ 500：服务器内部错误
+ 502：网关错误
+ 504：请求超时

## HTTPS 超文本传输安全协议
HTTP+SSL=HTTPS

HTTPS的好处：

1、HTTP是明文传输，HTTPS经过SSL\TLS加密传输

2、HTTP是无状态的，HTTPS可进行身份验证

HTTPS主要用于建设一个信息安全的通道，保证数据传输的安全性，同时御用验证网站的真实性，避免钓鱼网站

> 2019/5/7
