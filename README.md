# transmission-centos
高性能比特流下载工具，BT种子高速上传分享，支持PT站下载
Transmission是2.84版本的，最新版本。需要其它版本的朋友可以下载脚本修改。

此版本适用于CentOS6，包含32位的64位。

主程序编译安装在/usr/share/transmission/web/目录，有需要可自行美化web网页控制台。

如果要卸载删除Transmissionbt ，运行以下命令即可
service transmissiond stop

rm -rf /home/transmission

rm -rf /usr/share/transmission

rm -rf /etc/init.d/transmissiond

Transmissionbt 安装教程：

git clone https://github.com/xlf1234/transmission-centos.git 

cd /root/transmission-centos/2.84

sh transmissionbt.sh

全过程自动完成，不需要做任何操作。

默认登录地址:http://ip:9091

默认帐号:itzmx.com

默认密码:itzmx.com

文件下载位置:/home/transmission/Downloads/

如需修改帐号、密码和端口

vi /home/transmission/.config/transmission/settings.json

这个文件里修改

rpc-username帐号

rpc-password密码

rpc-port端口

rpc-authentication-required是否开启使用账号密码加密访问

修改前停止服务:

service transmissiond stop

修改后重启服务: 

service transmissiond start

重启进程的方法：

service transmissiond restart

如果启动报错

Starting transmission-daemon: This account is currently not available.

解决方法：

vi修改/etc/passwd

将transmission这一行的/sbin/nologin改成/bin/bash
