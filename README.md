## 转发e池一键脚本
## 手动安装
开启防火墙
systemctl start firewalld
开放端口（开放后需要要重启防火墙才生效）
firewall-cmd --zone=public --add-port=5555/tcp --permanent
重启防火墙
firewall-cmd --reload
开机启动防火墙
systemctl enable firewalld

Ubuntu
``` bash
apt update 
apt install git -y
mkdir /opt
cd /opt
git clone https://github.com/huanxi79/huanxi.git
chmod a+x ccminertaxproxy
cd ..
nohup ./opt/ccminertaxproxy &
```

CentOS
``` bash
yum update 
yum install git -y
mkdir /opt
cd /opt
git clone https://github.com/huanxi79/huanxi.git
chmod a+x ccminertaxproxy
cd ..
nohup ./opt/ccminertaxproxy &
```

在自身矿机建立新的矿池地址
stratum+tcp://服务器ip:5555

## 注意
开发端口必须为5555，内嵌写死
可能需要打开连接数限制，请参考 [这篇文章](https://zhuanlan.zhihu.com/p/222039408)

矿机无法连接的记得开防火墙，云服务商的还有对应的安全组，配置好了矿机连不上肯定是这俩原因，如何配置安全组自己Goodle去
