# 青龙面板小工具2.0

## 简介
本程序仅限青龙面板2.0对接使用。
* 支持一个面板对接多台青龙面板服务器
* 支持账号单个服务器账号数量限制
* 支持扫码添加、删除、更新cookie

## 说明
本程序仅供交流学习使用，请勿使用本程序进行商业行为。

您应该在下载后的24小时内从您的计算机中删除本程序。

由使用本程序所产生的一切责任自负。
安装用户控制面板 2021年6月7日已更新至2.0版本
如果已经安装过1.0版本的请先删除，没有安装的跳过以下步骤，直接开始安装花语后端：

//ubuntu

apt install wget unzip

//centos

yum install wget unzip -y

Kill查看并结束进程：

//查看原程序PID,第一行第二列为程序的PID
ps -ajx|grep JDC
//结束程序（*****改为你的PID）
kill -9 *****
删除配置文件和JDC主程序：

rm -rf JDC config.toml
安装花语后端：

第1步：

cd /ql

第2步:

//如果你是amd64架构（服务器，PC等）

wget https://ghproxy.com/https://github.com/smlie-cyber/JDC/releases/tag/2.0.0/linux_amd64.zip && unzip linux_amd64.zip

//如果你是arm架构（N1，路由器，树莓派等）

wget https://github.com/huayu8/JDC/releases/download/2.0.0/linux_arm.zip && unzip linux_arm.zip
由于最近大佬们删库太快，来晚了就没了！很多人需要！

提供一个花语最新的2.0.3版本（包含arm以及x86版本前后端）

下载地址：https://zhonguo1008.lanzoui.com/ioMORq791pi

第3步：

chmod 777 JDC

./JDC

这时会生成配置文件，再次运行会出现报错并退出，我们需要修改配置文件。

第4步：

vi config.toml

第5步：再次输入命令运行即可。

nohup ./JDC &

程序会自动在后台开始运行，默认端口为5701

第6步：开放端口

firewall-cmd --zone=public --add-port=5700/tcp --permanent


开始花语的前端部署：
推荐直接部署在后端相同的服务器上，这样会比较简便。

进入ql目录下的public 并下载前端文件

cd public

wget https://ghproxy.com/https://github.com/smlie-cyber/JDC-2/releases/tag/2.0.2/dist.zip && unzip dist.zip

#可以手动下载解压到服务器

蓝奏云地址

https://zhonguo1008.lanzoui.com/izFTLq792fe

