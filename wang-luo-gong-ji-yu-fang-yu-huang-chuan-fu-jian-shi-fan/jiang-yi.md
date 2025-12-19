# 讲义

1.2 网络技术回顾

什么是网络

网络是由节点和连线构成的，表示诸多对象及其相互联系，比如常见的计算机网络，通信网络，交通网络，广播电视网络，人际关系网络等。

什么是计算机网络

一些相互连接的、以共享资源为目的的、自治的计算机的集合。

基本的计算机网络系统包含：计算机网络操作系统、计算机硬件、计算机软件、交换机路由器等连接设备、网络协议。

能被我们用传统搜索引擎，搜索到的信息所在的网络为表层网，找不到的深网，最深沉是暗网。本门课表层网。



<figure><img src="../.gitbook/assets/Screenshot 2025-12-15 at 11.12.13 am.png" alt=""><figcaption></figcaption></figure>

同时在不同层次建立统一的标准，即网络协议，能够让网络更加开放。

国家标准是七层。

互联网上是4层。网络接口、网络层、传输层、应用层。

TCP/IP 四层模型中：（1）网络接口层：该层处于实际的计算机网络硬件（如网卡）之上，利用以太网中的数据链路进行通信 (2)网络层：IP协议的作用，将分组数据包发送到目的主机。ICMP:IP 数据包发送过程中一旦发生异常导致无法到达对端目标地址时，需要给发送端一个发生异常的通知，

传输层：让应用程序之间实现通信。 TCP协议：面向有链接的传输层协议，可以保证通信两端主机之间的通信可达，可以正确的处理传输过程中的丢包、传输乱序等异常情况；还能有效利用带宽，缓解网络拥堵。UDP协议：面向无连接的传输层协议，不关注对端是否真的收到传送的数据。应用层。提供服务的程序叫服务端。接受服务的程序叫客户端。服务器预先部署到主机上。等待接受任何时刻客户端发送到请求。

2.1 什么是网络安全

网络安全：一般指的是网络系统的硬件、软件及其系统中的数据收到保护，不因偶然的或者恶意的原因而遭受到破坏、更改、泄漏，系统连续可靠正常地运行。网络服务不间断。网络设备安全，信息安全，软件安全等。![](<../.gitbook/assets/Screenshot 2025-12-15 at 11.33.57 am.png>)

由于近年来网络安全日益凸显，我国将网络安全问题提升为国家层次的安全战略问题。由此网络安全进一步延伸成为网络空间安全。

网络空间安全（Cyberspace)：一般指的是信息环境中的一个整体域，它由独立相互依存的信息基础设施和网络组成。

网络空间包括互联网、电信网、计算机系统、嵌入式处理器、控制器系统。网络空间是人的生存空间，也是信息的生存环境。网络空间安全是人和信息对网络空间的基本要求。网络空间是所有信息系统的集合，而且复杂的巨系统，人在其中与信息相互作用、相互影响，

不安全的代码会造成系统的不安全，从而导致安全事件的发生。

3.1 什么是网络攻防技术

<figure><img src="../.gitbook/assets/Screenshot 2025-12-19 at 11.21.52 am.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-19 at 11.22.34 am.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-19 at 11.23.00 am.png" alt=""><figcaption></figcaption></figure>

网络攻防技术：（1）主动攻击（2）被动攻击

主动攻击：对被害者的消息进行更改或者拒绝用户使用资源的攻击方式。包括篡改信息、伪造信息、拒绝服务等。

篡改信息：一个合法消息的某些部分未经授权被改变、删除，或者是消息被延迟、改变顺序等行为。

伪造：某个实体（人或系统）发出含有其他实体身份嘻嘻等数据信息，假扮成其他实体，从而以欺骗方式获取一些合法用户的权利和特权的行为。

拒绝服务：DOS, 该行为会导致对通讯设备正常使用或管理被无条件地中断。

主动攻击无法防止。一般通过过滤和jiance

&#x20; 抗击主动攻击：（1） 过滤：将外网流入内网的可疑消息直接丢弃，而不让其进入内网。比如防火墙

<figure><img src="../.gitbook/assets/Screenshot 2025-12-19 at 11.32.48 am.png" alt=""><figcaption></figcaption></figure>

检测：对内网中可疑消息进行判断或评估的方法，在一定程度上也能起到防止攻击的作用。具体措施包括自动审计、入侵检测和完整性恢复等。

被动攻击：攻击者不对数据信息做任何修改，但在未经授权用户同意与认可的情况下截取或者窃听授权用户的信息或者相关信息。通常包括窃听、流量分析等攻击方式，

<figure><img src="../.gitbook/assets/Screenshot 2025-12-19 at 11.36.41 am.png" alt=""><figcaption></figcaption></figure>

如果信息没有采取加密措施，那么窃听者就可以完全掌握通信等全部内容。

无线截获方式：

流量分析：攻击者虽然从截获的消息中无法的到消息的真实内容，但攻击者还能通过观察这些数据报的模式，分析确定出通信双方的位置、通信的次数及消息的长度，获知相关的敏感消息。由于被动攻击不会对被攻击的信息作任何修改，基本不留攻击痕迹，很难检测。重点预防。被动攻击作为主动攻击的前奏。

&#x20;攻防位置：本地攻击和远程攻击

本地攻击：攻击者可以物理接触被害者的主机，并对该主机实施攻击的行为。远程攻击：攻击者通过网络对被害者进行攻击的行为。具体还可分为服务方攻击、客户端攻击与中间人攻击。

服务方攻击（Server-side Attack):攻击者对被害者主机的各种网络服务（web,ftp,telnet等）进行攻击的行为。

<figure><img src="../.gitbook/assets/Screenshot 2025-12-19 at 11.49.47 am.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-19 at 11.50.07 am.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-19 at 11.52.12 am.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-19 at 11.57.42 am.png" alt=""><figcaption></figcaption></figure>

无论用户输入什么密码都将成功登陆系统。

<figure><img src="../.gitbook/assets/Screenshot 2025-12-19 at 12.03.58 pm.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-19 at 12.05.41 pm.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-19 at 12.06.07 pm.png" alt=""><figcaption></figcaption></figure>

&#x20; 如果用户提交的是这个语句

<figure><img src="../.gitbook/assets/Screenshot 2025-12-19 at 12.06.28 pm.png" alt=""><figcaption></figcaption></figure>

这说明，该网页存在xss漏洞。能嵌入代码并执行，

z















