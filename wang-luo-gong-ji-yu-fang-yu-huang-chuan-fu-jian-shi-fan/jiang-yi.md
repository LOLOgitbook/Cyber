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

主动攻击无法防止。一般通过过滤和检测

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

<figure><img src="../.gitbook/assets/Screenshot 2025-12-19 at 3.07.38 pm.png" alt=""><figcaption></figcaption></figure>

拒绝服务攻击：拒绝服务攻击是一种简单的破坏性攻击。通常是利用传输协议中的某个弱点或者是系统存在的漏洞、或者服务漏洞，对目标系统发起大规模的进攻，用超出目标处理能力的海量数据包消耗可用的系统资源、带宽资源等， 或造成程序缓冲区溢出错误，致使其无法处理合法用户的正常请求，从而无法提供正常服务，最终导致网络服务瘫痪甚至是系统死机。&#x20;

TCP三次握手：

<figure><img src="../.gitbook/assets/Screenshot 2025-12-19 at 3.12.56 pm.png" alt=""><figcaption></figcaption></figure>

Synflood 攻击

&#x20;欺骗攻击：实质上就是一种冒充身份通过认证骗取信任的攻击方式

<figure><img src="../.gitbook/assets/Screenshot 2025-12-19 at 3.18.04 pm.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-19 at 3.18.28 pm.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-19 at 3.27.52 pm.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-19 at 3.39.13 pm.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-19 at 3.41.25 pm.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-19 at 3.41.49 pm.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-19 at 3.44.34 pm.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-19 at 3.46.09 pm.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-19 at 3.46.55 pm.png" alt=""><figcaption></figcaption></figure>

3.3 网络攻击发展

（1）越来越不对称的威胁

因特网上的安全是相互依赖的。

（2） 攻击工具越来越复杂

攻击工具三个特点：

<figure><img src="../.gitbook/assets/Screenshot 2025-12-19 at 4.16.12 pm.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-19 at 4.17.50 pm.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-19 at 4.19.00 pm.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-19 at 4.19.50 pm.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-19 at 4.21.08 pm.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-19 at 4.21.46 pm.png" alt=""><figcaption></figcaption></figure>



<figure><img src="../.gitbook/assets/Screenshot 2025-12-22 at 10.58.01 am.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-22 at 11.01.44 am.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-22 at 11.02.09 am.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-22 at 11.02.49 am.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-22 at 11.03.15 am.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-22 at 11.08.24 am.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-22 at 11.08.42 am.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-22 at 11.09.14 am.png" alt=""><figcaption></figcaption></figure>

一个路由器是一个传统的网络级防火墙，路由器检查这些信息来决定是否将所有的包转发，但是不能判断出一个ip包来自何方，去向何处。应用级网关：应用级网关能够检查进出的数据包，通过网关复制传递数据，防止在受信任服务器和客户机与不受信任的主机间直接建立联系。

<figure><img src="../.gitbook/assets/Screenshot 2025-12-22 at 11.17.25 am.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-22 at 11.18.24 am.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-22 at 11.21.11 am.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-22 at 11.36.26 am.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-22 at 11.38.13 am.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-22 at 11.38.21 am.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-22 at 11.38.46 am.png" alt=""><figcaption></figcaption></figure>

3.5 网络巩防竞赛：CTF.

<figure><img src="../.gitbook/assets/Screenshot 2025-12-22 at 11.42.20 am.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-22 at 11.44.29 am.png" alt=""><figcaption></figcaption></figure>

4.1 网络攻击技术的一般步骤

（1）确定攻击目标，（2）信息收集 （3）获取用户权限 （4）安装后门（5）扩大影响（6）清除痕迹



<figure><img src="../.gitbook/assets/Screenshot 2025-12-22 at 11.49.17 am.png" alt=""><figcaption></figcaption></figure>

信息收集的主要方法：利用公开信息服务收集信息。通过主机扫描与端口扫描手机系统信息。通过操作系统探测与应用程序类型识别收集系统与应用程序信息。

获取用户权限：口令攻击、缓冲区溢出、脚本攻击等。

安装后门：通过上传木马实现对目标的控制

扩大影响：使用远程攻击方式攻击，使用局域网内部攻击所特有的嗅探、假信息攻击等方法实施攻击。

清除痕迹：rootkit隐藏 和系统安全日志消除。

4.2.1 网络踩点

攻击前奏：（1）确定攻击目标（2）为后继攻击做准备：进行信息收集

<figure><img src="../.gitbook/assets/Screenshot 2025-12-22 at 3.55.13 pm.png" alt=""><figcaption></figcaption></figure>

对对手信息的掌握是能够取胜的关键。在实施攻击前，需要收集什么样的信息呢？

尽可能多的收集目标信息。

<figure><img src="../.gitbook/assets/Screenshot 2025-12-22 at 3.59.00 pm.png" alt=""><figcaption></figcaption></figure>

在一个渗透项目下，你需要有多次的信息收集，同时也要运用不同的收集方式，才能保证信息收集的完整性。

信息收集：网络踩点，网络扫描，网络查点

（1）网络踩点：在攻击前通过网络搜索来获取目标公开信息的一种手段。 通过web信息搜索与挖掘，DNS与IP查询，网络拓扑侦查。

<figure><img src="../.gitbook/assets/Screenshot 2025-12-22 at 4.04.43 pm.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-22 at 4.07.14 pm.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-22 at 4.07.33 pm.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-22 at 4.10.55 pm.png" alt=""><figcaption></figcaption></figure>

通过域名注册信息查询可以获取注册人的详细注册信息，

<figure><img src="../.gitbook/assets/Screenshot 2025-12-22 at 4.12.06 pm.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-22 at 4.12.54 pm.png" alt=""><figcaption></figcaption></figure>

&#x20;  通过host获取企业ip地址。近期DNS服务商等企业已经对公开信息进行了一定程度的屏蔽。为了防止攻击者从公开信息中获取敏感情报。

<figure><img src="../.gitbook/assets/Screenshot 2025-12-22 at 4.14.57 pm.png" alt=""><figcaption></figcaption></figure>

我们用tracert来跟踪目标地址的IP。

<figure><img src="../.gitbook/assets/Screenshot 2025-12-22 at 4.15.40 pm.png" alt=""><figcaption></figcaption></figure>

与该目标同属一个网段内，还有两个主机。

4.2.2 网络扫描技术

<figure><img src="../.gitbook/assets/Screenshot 2025-12-22 at 4.24.05 pm.png" alt=""><figcaption></figcaption></figure>

网络扫描通常分为服务扫描、端口扫描以及批量扫描。

服务扫描：对目标进行www服务的扫描

<figure><img src="../.gitbook/assets/Screenshot 2025-12-22 at 4.30.04 pm.png" alt=""><figcaption></figcaption></figure>



<figure><img src="../.gitbook/assets/Screenshot 2025-12-22 at 4.30.35 pm.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-22 at 4.31.05 pm.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-22 at 4.31.31 pm.png" alt=""><figcaption></figcaption></figure>

常见的网络扫描技术：

<figure><img src="../.gitbook/assets/Screenshot 2025-12-22 at 4.33.16 pm.png" alt=""><figcaption></figcaption></figure>

TCP连接扫描技术优点：1. 不需要任何权限，系统中的任何用户都有权利使用这个调用。2.实现简单、稳定可靠。缺点：扫描方式不隐蔽、很容易被发觉。服务器日志会记录下大量的密集的连接和错误记录，容易被防火墙发现屏蔽。

<figure><img src="../.gitbook/assets/Screenshot 2025-12-22 at 4.35.37 pm.png" alt=""><figcaption></figcaption></figure>

优点：不容易被发现。缺点：在大部分操作系统中，发送主机需要构造适用于这种扫描的IP包，通常情况下，构造SYN数据包需要超级用户或者得到授权的用户，才能访问专门的系统调用。

<figure><img src="../.gitbook/assets/Screenshot 2025-12-22 at 4.38.08 pm.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-22 at 4.39.29 pm.png" alt=""><figcaption></figcaption></figure>

秘密扫描：利用UDP端口关闭时返回的ICMP信息，不包含标准的TCP上次握手协议的任何部分，隐蔽性好。

<figure><img src="../.gitbook/assets/Screenshot 2025-12-22 at 4.42.17 pm.png" alt=""><figcaption></figcaption></figure>

ICMP扫描

<figure><img src="../.gitbook/assets/Screenshot 2025-12-22 at 4.43.59 pm.png" alt=""><figcaption></figcaption></figure>

PING程序一般是直接实现在系统内核中的。利用ICMP实现的。

利用最基本的报错功能。如果接收到的数据包协议项出现了错误，那么接收端将产生一个Destination Unreachable ICMP的错误报文。如果向目标主机发送一个特殊的IP数据包，比如异常的IP头长度，目标主机将返回“Parameter Problem"的ICMP错误报文。

防火墙，过滤设备。

4.2.3.网络查点技术

网络查点：根据网络扫描的结果进一步地对目标主机的服务以及系统版本等信息进行更针对性的检测，来寻找真正可以攻击的入口，以及攻击过程中可能需要的关键数据。

（1）服务判定：根据端口判定

<figure><img src="../.gitbook/assets/Screenshot 2025-12-25 at 11.19.00 am.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-25 at 11.19.26 am.png" alt=""><figcaption></figcaption></figure>

（2）网络服务旗标（banner）抓取技术

（3）操作系统指纹识别技术：许多安全漏洞都依赖于操作系统及其版本，如果没有这些信息，攻击者的攻击将失去攻击的方向

<figure><img src="../.gitbook/assets/Screenshot 2025-12-25 at 11.24.09 am.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-25 at 11.24.25 am.png" alt=""><figcaption></figcaption></figure>

嗅探工具

<figure><img src="../.gitbook/assets/Screenshot 2025-12-25 at 11.25.28 am.png" alt=""><figcaption></figcaption></figure>

4.2.4 网络监听技术

<figure><img src="../.gitbook/assets/Screenshot 2025-12-25 at 11.26.33 am.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-25 at 11.27.15 am.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-25 at 11.28.00 am.png" alt=""><figcaption></figcaption></figure>

基于共享式局域网的监听技术：监听者通过网卡获取同属于一个共享式局域网中所有其他主机发送的数据包的技术。

基于交换式局域网的监听技术：监听者通过欺骗等方式来获取同属于一个局域网中其他主机发送的数据的技术。

溢出攻击：交换机工作时要维护一张MAC地址与端口的映射表。用于维护这种表的内存是有限的，如果用大量的错误的MAC地址的数据帧对交换机进行攻击，交换机可能出现溢出，这时交换机就会退回到集线器的广播方式，向所有的端口发送数据包。

ARP欺骗：计算机中维护着一个IP-MAC地址对应表，记录了IP地址和MAC地址之间的对应关系。

4.3.1口令攻击技术

常见攻击技术：

1\. 口令攻击

口令的作用就是向系统提供唯一标识个体身份的机制，只给个体所需信息的访问权，从而达到保护敏感信息和个人隐私的作用。

<figure><img src="../.gitbook/assets/Screenshot 2025-12-25 at 11.51.53 am.png" alt=""><figcaption></figcaption></figure>

多数管理员想保证他们自己不被所在系统之外，一种方法就是创建一个口令非常容易记忆的账号；另一种方法就是和别人共享口令或者把它写下来。

<figure><img src="../.gitbook/assets/Screenshot 2025-12-25 at 11.57.38 am.png" alt=""><figcaption></figcaption></figure>

具体的攻击方式有：词典攻击、强行攻击以及组合攻击。

（1）词典攻击：词典是一个单词列表文件，使用一个或多个词典文件，利用里面的单词列表进行口令猜测的过程，就是词典攻击。(2)强行攻击：

<figure><img src="../.gitbook/assets/Screenshot 2025-12-25 at 12.06.15 pm.png" alt=""><figcaption></figcaption></figure>

系统的一些限定条件将有助于强行攻击破解口令。

分布式暴力破解：

组合攻击：在使用词典单词的基础上在单词的后面串接几个字母和数字进行攻击的攻击方式。（4）其他方式：

口令破解

<figure><img src="../.gitbook/assets/Screenshot 2025-12-25 at 12.10.01 pm.png" alt=""><figcaption></figcaption></figure>

4.3.2 缓冲区溢出攻击

缓冲区：包含相同数据类型实例的一个连续的计算机内存块，是3434程序运行期间在内存中分配的一个连续的区域，用于保存包括字符数组在内的各种数据类型。

溢出：所填充的数据超出了原有的缓冲区边界。

<figure><img src="../.gitbook/assets/Screenshot 2025-12-25 at 3.45.17 pm.png" alt=""><figcaption></figcaption></figure>

缓冲区溢出攻击原因：各种操作系统和应用软件上存在的缓冲区溢出问题数不胜数。

缓冲区溢出漏洞攻击的危害：1. 导致程序运行失败、系统崩溃以及重新启动。2.利用缓冲区溢出执行非授权指令，甚至取得系统特权，进而进行各种非法操作。

防御网络入侵以及入侵检测的重点之一：如何防止和检测出利用缓冲区溢出漏洞进行的攻击。

溢出攻击原理：

<figure><img src="../.gitbook/assets/Screenshot 2025-12-25 at 3.50.54 pm.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-25 at 3.51.18 pm.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-25 at 3.51.46 pm.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-25 at 3.52.02 pm.png" alt=""><figcaption></figcaption></figure>

产生溢出。

堆溢出的工作方式与栈溢出的工作方式的不同的：堆没有压栈和入栈操作，而是分配和回收内存。

<figure><img src="../.gitbook/assets/Screenshot 2025-12-25 at 3.56.54 pm.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-25 at 3.57.11 pm.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-25 at 3.59.00 pm.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-25 at 3.59.22 pm.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Screenshot 2025-12-25 at 3.59.29 pm.png" alt=""><figcaption></figcaption></figure>

&#x20;

<figure><img src="../.gitbook/assets/Screenshot 2025-12-25 at 4.00.12 pm.png" alt=""><figcaption></figcaption></figure>

4.3.3. 木马攻击

<figure><img src="../.gitbook/assets/Screenshot 2025-12-25 at 4.01.24 pm.png" alt=""><figcaption></figcaption></figure>

木马具有很强的隐蔽性，木马特点：有效性、隐蔽性、顽固性、易植入性

<figure><img src="../.gitbook/assets/Screenshot 2025-12-25 at 4.03.26 pm.png" alt=""><figcaption></figcaption></figure>

&#x20;隐蔽性：木马必须有能力长期潜伏于目标机器中而不被发现。一个隐蔽性差的木马往往会很容易被杀毒软件





&#x20;





