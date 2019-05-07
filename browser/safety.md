# web安全
### XSS
XSS，跨站脚本攻击，cross-site script，攻击原理是攻击者向存在漏洞的网页注入恶意的HTML代码，当用户浏览网页时，恶意代码会自动执行，从而发动攻击，如盗取用户cookie，破坏网页结构重定向到其他网站等；

防御措施：过滤用户输入的内容，对用户输入做转义处理

### csrf
csrf，跨站请求伪造，cross-site request forgrey，攻击者盗取用户信息，以用户名义向网站发起恶意请求；

防御措施：post、验证码、token

> 2019/5/7