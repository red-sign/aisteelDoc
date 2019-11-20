# Application 存储
该面板主要是记录网站加载的所有资源信息，包括存储数据（LocalStorage、SessionStorage、IndexedDB、Web SQL、Cookies）、缓存数据、字体、图片、脚本、样式表等。
常用的是浏览器本地存储`LocalStorage`、`SessionStorage`，还有`Cookies`。

![本地存储](assets/001/004-1573114800805.png)

> 为了安全，不同域名或端口号的存储不能通用。例如在`aisteel.com`存储的数据，在`om.aisteel.com`无法访问。
> 同理，同一浏览器域名和端口号相同时，即使时不同窗口，存储也是通用的。所以在不同窗口登录不同账号，后登录的会将之前登录的信息覆盖导致之前登录的账号状态异常。

## LocalStorage 
长期存储，关闭网页或浏览器不会导致数据消失。例如存储用户的登录信息（用户名username、用户vid、token等）。双击键或值也可以修改对应的内容（不建议修改）

![存储操作示意](assets/001/004-1573115328819.png)

> 什么是token：Token是服务端生成的一串字符串，以作客户端进行请求的一个令牌，当第一次登录后，服务器生成一个Token字符串便将此字符串返回给客户端，以后客户端只需带上这个Token前来请求数据即可，即证明该用户已经登录。


## SessionStorage
短期操作，关闭浏览器数据即消失。例如存储网页跳转时所用的数据（订单id等）。存储的操作与LocalStorage相同


