#使用CC攻击器进行DDos攻击实验报告

##一、实验目的

1.通过练习使DDoS攻击工具对目标主机进行攻击;

2.理解DDoS攻击的原理及其实施过程；

3.掌握检测和防范DDoS攻击的措施。

##二、实验原理

DDos原理
   
   
       分布式拒绝服务（DosDoS）是基于DoS攻击的一种特殊形式。攻击者将多台受控制的计算机联合起来向目标计算机发起DoS攻击。 
       DDoS攻击分为3层：攻击者、主控端、代理端。
         1、攻击者：攻击者所用的计算机是攻击主控台，攻击者操纵整个攻击过程，它向主控端发送攻击命令。
         2、主控端：主控端是攻击者非法侵入并控制的一些主机，这些主机还分别控制大量的代理主机。主控端主机的上面安装了特定的程序，因此它们可以接受攻击者发来的特殊指令，并且可以把这些命令发送到代理主机上。
         3、代理端：代理端同样也是攻击者侵入并控制的一批主机，它们上面运行攻击器程序，接受和运行主控端发来的命令。代理端主机是攻击的执行者，真正向受害者主机发送攻击。
        攻击者发起DDoS攻击的第一步，就是寻找在Internet上有漏洞的主机，进入系统后在其上面安装后门程序，攻击者入侵的主机越多，他的攻击队伍就越壮大。第二步在入侵主机上安装攻击程序，其中一部分主机充当攻击的主控端，一部分主机充当攻击的代理端。最后各部分主机各司其职，在攻击者的调遣下对攻击对象发起攻击。
        
CC攻击器攻击原理
    
       CC(ChallengeCollapsar)攻击的原理就是攻击者控制某些主机不停地发大量数据包给对方服务器造成服务器资源耗尽，一直到宕机崩溃。CC主要是用来攻击页面的，每个人都有这样的体验：当一个网页访问的人数特别多的时候，打开网页就慢了，CC就是模拟多个用户（多少线程就是多少用户）不停地进行访问那些需要大量数据操作（就是需要大量CPU时间）的页面，造成服务器资源的浪费，CPU长时间处于100%，永远都有处理不完的连接直至就网络拥塞，正常的访问被中止。
       

##三、使用CC攻击器进行攻击实验

        实验使用小白超强CC攻击器V1.0
        
        1.配置自己为攻击目标。发给10.11.1.145运行程序。在其系统进程中创建了ddostest.exe，并对配置的目标发起了攻击。
        2.通过netstat –ano查看端口连接。
        3. 在netstat –ano下查看到建立网络连接的进程Pid号。 然后tasklist查看PID号对应的进程。
        4.使用wireshark分析数据包。
##四、实验心得

        通过本次实验主要学会了使用DDoS攻击工具对目标主机进行攻击；进一步理解了DDoS攻击的原理及其实施过程；并掌握了检测和防范DDoS攻击的措施。希望本次实验会给以后的学习带来帮助。
        
##五、实验截图

![alt text](https://raw.githubusercontent.com/kadaokaduan/ns/master/2015-2/manhongpeng_taorui_zuotianyi/11.png "实验截图1")

![alt text](https://raw.githubusercontent.com/kadaokaduan/ns/master/2015-2/manhongpeng_taorui_zuotianyi/22.png "实验截图2")

![alt text](https://raw.githubusercontent.com/kadaokaduan/ns/master/2015-2/manhongpeng_taorui_zuotianyi/33.png "实验截图3")