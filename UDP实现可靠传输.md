<title>UDP实现可靠传输协议</title>
#UDP实现可靠传输协议
<a href="http://blog.codingnow.com/2016/03/reliable_udp.html">参考网址1</a>

想要UDP实现TCP的可靠传输，同时又比TCP响应速度快，一定是放弃了TCP
的一些保障，换取在特定情况下的优势。

###一种想法
1. 业务逻辑上允许信息丢失，比如如果收到新的全部状态信息就不需要旧的状态信息。
2. 允许包乱序，能够允许包乱序的场景可以是一问一答的请求回应，比如DNS查询，数据量小，UDP最大512字节，对于一般DNS查询足够了。

