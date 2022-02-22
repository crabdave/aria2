# aria2
aria2 download tool

# CentOS 7


yum install -y epel-release
yum install -y aria2

修改字符集 UTF-8


cat /root/aria2/aria2.conf
aria2安装参考链接：https://blog.csdn.net/never_late/article/details/113405878


# -------------------------------ariang docker---------------------------
docker run -d \
    --name ariang \
    --restart unless-stopped \
    -p 6880:6880 \
    p3terx/ariang

ariang 参考链接：https://p3terx.com/archives/aria2-frontend-ariang-tutorial.html
    


# ---------------------------------过一会再启动aira2服务----------------------

aria2c --conf-path=/root/aria2/aria2.conf -D
ps -ef |grep aria

# ---------------------------------在界面配置中修改密钥-----------------------
http://你的ip地址:6880
AriaNg 设置
         ------------------Aria2 RPC 密钥
crabdave

# ----------------------------------------------------------------------------
TIPS: 无法连接一般是两种情况导致的：1. 6800 端口未开放。 2. 网络不通畅。

# ---------------------------------防火墙打开6800端口-------------------------
firewall-cmd --add-port=6800/tcp --permanent
firewall-cmd --reload


