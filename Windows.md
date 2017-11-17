# Windows

### 网络

- 局域网内，本机可以ping通其他主机，其他主机ping不通本机。原因时防火墙ICMPv4公用配置没有启用。解决方法：
  > 防火墙 == 高级 == 入站规则 == 按照协议排序 == 回显请求 ICMPv4-In 公用 == 启用

- 在查找Windows如何为主机启用IP Forwarding时，找到了这个文档: [TCP/IP Fundamentals for Microsoft Windows][1].
  帮助我发现的[链接][2]，另一个指导[链接][3]


[1]: doc/TCPIP_Fund.pdf
[2]: https://social.technet.microsoft.com/Forums/windows/en-US/35b00eb7-aa2d-4543-8774-b618da27b6cd/attempting-to-configure-ip-routing-on-windows-7-pro-question?forum=w7itpronetworking
[3]: https://answers.microsoft.com/en-us/windows/forum/windows_7-networking/how-to-enable-ip-routing-in-windows-7/8970e722-e947-460d-80d5-fd6ffc850f3f