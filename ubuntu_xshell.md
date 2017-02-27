### ubuntu 与 xshell 连接问题总结

#### 在linux中 ifconfig命令

* 如果有ip地址则如下

![][ifconfig]

* 如果还是连不上并且没有手动ssh点击下面的连接 

	* [如何在Ubuntu中安装ssh服务][如何在Ubuntu中安装ssh服务]

* 当完成上面的步骤时要确认

![][允许root远程登录]

* 不过此时有可能普通用户可以登录而登录root是会出现

![][ssh拒绝了您的密码]

> 这是由于默认root密码是随机的，即每次开机都有一个新的root密码。

* 这时我们需要

![][修改root密码]

* :snake:这时就可以用普通用户和root用户登录linux了

* 此外还有一点:

创建新用户时

1. 用root账号密码登录linux系统

2. 用useradd oldboy（用户名）

3. 用passwd oldboy (之后修改密码)

4. 用passwd 是修改root密码


<!-- 下面是链接引用-->

[ifconfig]: images/ifconfig.jpg
[如何在Ubuntu中安装ssh服务]:http://jingyan.baidu.com/article/9c69d48fb9fd7b13c8024e6b.html
[允许root远程登录]: images/root_alow.jpg
[ssh拒绝了您的密码]: images/error_passwd.jpg
[修改root密码]: images/passwd.jpg
