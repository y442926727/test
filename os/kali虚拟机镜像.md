kali虚拟机镜像

网络问题

虚拟机启动net网络ipv6

修改 /etc/apt/sources.list , 将相关 url 改成阿里云的源。

```bash
#deb https://mirrors.aliyun.com/kali kali-rolling main non-free contrib
#deb-src https://mirrors.aliyun.com/kali kali-rolling main non-free contrib
```

```bash
apt-get update  # 取回更新的软件包列表信息
apt-get upgrade # 进行一次升级
apt-get clean # 删除已经下载的安装包
reboot  #重启
```

Ubuntu有两种类型的软件包：二进制软件包（deb）和源码包（deb-src）

1、二进制软件包（Binary Packages）：它包含可执行文件、库文件、配置文件、man/info页面、版权声明和其它文档。

2、源码包（Source Packages）：包含软件源代码、版本修改说明、构建指令以及编译工具等。先由tar工具归档为.tar.gz文件，然后再打包成.dsc文件。

在用户不确定一个软件包类型时，可以使用file命令查看文件类型。

https://www.cnblogs.com/sanwumanzi/p/10521529.html

[Debian 9 中设置网络](https://www.cnblogs.com/samgg/p/7712136.html)

```bash
vim /etc/NetworkManager/NetworkManager.conf
service network-manager start
```

https://www.fujieace.com/kali-linux/device-not-managed.html

```bash
apt-get install ttf-wqy-micohei ttf-wqy-zenhei xfonts-wqy
dpkg-reconfigure locales
```

2019kali安装以及汉化