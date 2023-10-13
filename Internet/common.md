## 1.键入网址到网页显示，期间发生了什么？

[键入网址到网页显示，期间发生了什么？](https://xiaolincoding.com/network/1_base/what_happen_url.html#_2-2-%E9%94%AE%E5%85%A5%E7%BD%91%E5%9D%80%E5%88%B0%E7%BD%91%E9%A1%B5%E6%98%BE%E7%A4%BA-%E6%9C%9F%E9%97%B4%E5%8F%91%E7%94%9F%E4%BA%86%E4%BB%80%E4%B9%88)

![image-20231008092240640](https://ericcoder-oss.oss-cn-hangzhou.aliyuncs.com/markdown_images/image-20231008092240640.png)

## 2.TCP 三次握手与四次挥手总结

[TCP 三次握手与四次挥手面试题](https://xiaolincoding.com/network/3_tcp/tcp_interview.html)

## 3.TCP和UDP的区别

[UDP 和 TCP 有什么区别呢？分别的应用场景是？](https://xiaolincoding.com/network/3_tcp/tcp_interview.html#udp-%E5%92%8C-tcp-%E6%9C%89%E4%BB%80%E4%B9%88%E5%8C%BA%E5%88%AB%E5%91%A2-%E5%88%86%E5%88%AB%E7%9A%84%E5%BA%94%E7%94%A8%E5%9C%BA%E6%99%AF%E6%98%AF)

## 4.为什么是三次握手？不是两次、四次？

[为什么是三次握手？不是两次、四次？](https://xiaolincoding.com/network/3_tcp/tcp_interview.html#%E4%B8%BA%E4%BB%80%E4%B9%88%E6%98%AF%E4%B8%89%E6%AC%A1%E6%8F%A1%E6%89%8B-%E4%B8%8D%E6%98%AF%E4%B8%A4%E6%AC%A1%E3%80%81%E5%9B%9B%E6%AC%A1)

TCP 建立连接时，通过三次握手**能防止历史连接的建立，能减少双方不必要的资源开销，能帮助双方同步初始化序列号**。序列号能够保证数据包不重复、不丢弃和按序传输。

不使用「两次握手」和「四次握手」的原因：

- 「两次握手」：无法防止历史连接的建立，会造成双方资源的浪费，也无法可靠的同步双方序列号；
- 「四次握手」：三次握手就已经理论上最少可靠连接建立，所以不需要使用更多的通信次数。

## 5.为什么挥手需要四次？

[为什么挥手需要四次？](https://xiaolincoding.com/network/3_tcp/tcp_interview.html#%E4%B8%BA%E4%BB%80%E4%B9%88%E6%8C%A5%E6%89%8B%E9%9C%80%E8%A6%81%E5%9B%9B%E6%AC%A1)

再来回顾下四次挥手双方发 `FIN` 包的过程，就能理解为什么需要四次了。

- 关闭连接时，客户端向服务端发送 `FIN` 时，仅仅表示客户端不再发送数据了但是还能接收数据。
- 服务端收到客户端的 `FIN` 报文时，先回一个 `ACK` 应答报文，而服务端可能还有数据需要处理和发送，等服务端不再发送数据时，才发送 `FIN` 报文给客户端来表示同意现在关闭连接。

从上面过程可知，服务端通常需要等待完成数据的发送和处理，所以服务端的 `ACK` 和 `FIN` 一般都会分开发送，因此是需要四次挥手。

## 6.HTTP请求常⻅的状态码和字段

[HTTP 常见的状态码有哪些？](https://xiaolincoding.com/network/2_http/http_interview.html#http-%E5%B8%B8%E8%A7%81%E7%9A%84%E7%8A%B6%E6%80%81%E7%A0%81%E6%9C%89%E5%93%AA%E4%BA%9B)

[HTTP 常见字段有哪些？](https://xiaolincoding.com/network/2_http/http_interview.html#http-%E5%B8%B8%E8%A7%81%E5%AD%97%E6%AE%B5%E6%9C%89%E5%93%AA%E4%BA%9B)

+ Host
+ Content-Length
+ Connection
+ Content-Type
+ Content-Encoding

## 7.GET和POST请求的区别

[GET 与 POST](https://xiaolincoding.com/network/2_http/http_interview.html#get-%E5%92%8C-post-%E6%9C%89%E4%BB%80%E4%B9%88%E5%8C%BA%E5%88%AB)

## 8.什么是强缓存和协商缓存

[什么是强制缓存？](https://xiaolincoding.com/network/2_http/http_interview.html#%E4%BB%80%E4%B9%88%E6%98%AF%E5%BC%BA%E5%88%B6%E7%BC%93%E5%AD%98)

[什么是协商缓存？](https://xiaolincoding.com/network/2_http/http_interview.html#%E4%BB%80%E4%B9%88%E6%98%AF%E5%8D%8F%E5%95%86%E7%BC%93%E5%AD%98)

## 9.HTTP1.0和HTTP1.1的区别？

![image-20231007183613837](https://ericcoder-oss.oss-cn-hangzhou.aliyuncs.com/markdown_images/image-20231007183613837.png)

## 10.HTTP2.0与HTTP1.1的区别？

![image-20231007183638536](https://ericcoder-oss.oss-cn-hangzhou.aliyuncs.com/markdown_images/image-20231007183638536.png)

## 11.HTTPS的⼯作原理？(https是怎么建⽴连接的）

[ HTTPS 是如何建立连接的？其间交互了什么？](https://xiaolincoding.com/network/2_http/http_interview.html#https-%E6%98%AF%E5%A6%82%E4%BD%95%E5%BB%BA%E7%AB%8B%E8%BF%9E%E6%8E%A5%E7%9A%84-%E5%85%B6%E9%97%B4%E4%BA%A4%E4%BA%92%E4%BA%86%E4%BB%80%E4%B9%88)

## 12.HTTPS与HTTP的区别

![image-20231007184309702](https://ericcoder-oss.oss-cn-hangzhou.aliyuncs.com/markdown_images/image-20231007184309702.png)

## 13.DNS是什么，及其查询过程

[ 真实地址查询 —— DNS](https://xiaolincoding.com/network/1_base/what_happen_url.html#%E7%9C%9F%E5%AE%9E%E5%9C%B0%E5%9D%80%E6%9F%A5%E8%AF%A2-dns)

> 域名解析的工作流程

1. 客户端首先会发出一个 DNS 请求，问 www.server.com 的 IP 是啥，并发给本地 DNS 服务器（也就是客户端的 TCP/IP 设置中填写的 DNS 服务器地址）。
2. 本地域名服务器收到客户端的请求后，如果缓存里的表格能找到 www.server.com，则它直接返回 IP 地址。如果没有，本地 DNS 会去问它的根域名服务器：“老大， 能告诉我 www.server.com 的 IP 地址吗？” 根域名服务器是最高层次的，它不直接用于域名解析，但能指明一条道路。
3. 根 DNS 收到来自本地 DNS 的请求后，发现后置是 .com，说：“www.server.com 这个域名归 .com 区域管理”，我给你 .com 顶级域名服务器地址给你，你去问问它吧。”
4. 本地 DNS 收到顶级域名服务器的地址后，发起请求问“老二， 你能告诉我 www.server.com 的 IP 地址吗？”
5. 顶级域名服务器说：“我给你负责 www.server.com 区域的权威 DNS 服务器的地址，你去问它应该能问到”。
6. 本地 DNS 于是转向问权威 DNS 服务器：“老三，www.server.com对应的IP是啥呀？” server.com 的权威 DNS 服务器，它是域名解析结果的原出处。为啥叫权威呢？就是我的域名我做主。
7. 权威 DNS 服务器查询后将对应的 IP 地址 X.X.X.X 告诉本地 DNS。
8. 本地 DNS 再将 IP 地址返回客户端，客户端和目标建立连接。

至此，我们完成了 DNS 的解析过程。现在总结一下，整个过程总结成了一个图。

![域名解析的工作流程](https://ericcoder-oss.oss-cn-hangzhou.aliyuncs.com/markdown_images/6.jpg)

## 14.HTTP多个TCP连接怎么实现

![image-20231007184440930](https://ericcoder-oss.oss-cn-hangzhou.aliyuncs.com/markdown_images/image-20231007184440930.png)

## 15.TCP 的 Keepalive 和 HTTP 的 Keep-Alive 是⼀个东⻄吗？

[TCP Keepalive 和 HTTP Keep-Alive 是一个东西吗？](https://xiaolincoding.com/network/3_tcp/tcp_http_keepalive.html)

HTTP 的 Keep-Alive 也叫 HTTP 长连接，该功能是由「应用程序」实现的，可以使得用同一个 TCP 连接来发送和接收多个 HTTP 请求/应答，减少了 HTTP 短连接带来的多次 TCP 连接建立和释放的开销。

TCP 的 Keepalive 也叫 TCP 保活机制，该功能是由「内核」实现的，当客户端和服务端长达一定时间没有进行数据交互时，内核为了确保该连接是否还有效，就会发送探测报文，来检测对方是否还在线，然后来决定是否要关闭该连接。

## 16.TCP连接如何确保可靠性

![image-20231007184658868](https://ericcoder-oss.oss-cn-hangzhou.aliyuncs.com/markdown_images/image-20231007184658868.png)

## 17.拥塞控制是怎么实现的

![image-20231007184823866](https://ericcoder-oss.oss-cn-hangzhou.aliyuncs.com/markdown_images/image-20231007184823866.png)

## 18.Cookie和Session是什么？有什么区别？

![image-20231007184919834](https://ericcoder-oss.oss-cn-hangzhou.aliyuncs.com/markdown_images/image-20231007184919834.png)

![image-20231007184928398](https://ericcoder-oss.oss-cn-hangzhou.aliyuncs.com/markdown_images/image-20231007184928398.png)

