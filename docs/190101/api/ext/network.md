# Network 扩展

代码|功能
:---:|:---:
`tcp`|TCP 套接字名称空间
`udp`|UDP 套接字名称空间
`string host_name()`|获取主机名

## TCP 套接字名称空间

代码|功能
:---:|:---:
`socket`|TCP 套接字类型
`[tcp::acceptor] acceptor([tcp::endpoint])`|在端点上建立接收器
`[tcp::endpoint] endpoint(string address,number port)`|在指定 IP 地址和端口上建立端点
`[tcp::endpoint] endpoint_v4(number port)`|在任意 IPv4 地址上和指定端口上建立端点
`[tcp::endpoint] endpoint_v6(number port)`|在任意 IPv6 地址上和指定端口上建立端点
`[tcp::endpoint] resolve(string host,string service)`|解析主机的服务并建立端点

## TCP 套接字类型扩展

代码|功能
:---:|:---:
`void connect([tcp::socket],[tcp::endpoint])`|连接到端点
`void accept([tcp::socket],[tcp::acceptor])`|接受一个 TCP 请求
`void close([tcp::socket])`|关闭套接字
`boolean is_open([tcp::socket])`|查询套接字是否打开
`string receive([tcp::socket],number buffer_size)`|接收一些数据,最大长度为 `buffer_size`
`void send([tcp::socket],string buffer)`|发送一些数据
`[tcp::endpoint] remote_endpoint([tcp::socket])`|获取远程端点

## TCP 端点类型扩展

代码|功能
:---:|:---:
`string address([tcp::endpoint])`|获取端点指向的地址
`number port([tcp::endpoint])`|获取端点指向的端口

## UDP 套接字名称空间

代码|功能
:---:|:---:
`socket`|UDP 套接字类型
`[udp::endpoint] endpoint(string address,number port)`|在指定 IP 地址和端口上建立端点
`[udp::endpoint] endpoint_v4(number port)`|在任意 IPv4 地址上和指定端口上建立端点
`[udp::endpoint] endpoint_v6(number port)`|在任意 IPv6 地址上和指定端口上建立端点
`[udp::endpoint] resolve(string host,string service)`|解析主机的服务并建立端点

## UDP 套接字类型扩展

代码|功能
:---:|:---:
`void open_v4([udp::socket])`|打开 IPv4 协议套接字
`void open_v6([udp::socket])`|打开 IPv6 协议套接字
`void bind([udp::socket],[udp::endpoint])`|将套接字绑定到端点上
`void close([udp::socket])`|关闭套接字
`boolean is_open([udp::socket])`|查询套接字是否打开
`string receive_from([udp::socket],number buffer_size,[udp::endpoint])`|从远程端点处接收一些数据,最大长度为 `buffer_size`
`void send_to([udp::socket],string buffer,[udp::endpoint])`|发送一些数据到远程端点

## UDP 端点类型扩展

代码|功能
:---:|:---:
`string address([udp::endpoint])`|获取端点指向的地址
`number port([udp::endpoint])`|获取端点指向的端口

**注意:**
+ TCP 套接字和 UDP 套接字的端点不能通用。
+ Network 扩展会抛出异常。