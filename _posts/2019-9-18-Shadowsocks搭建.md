---
layout:     post                       # 使用的布局（不需要改）
title:      Shadowsocks搭建                # 标题 
subtitle:   在VPS上搭建Shadowsocks #副标题
date:       2019-9-18                 # 时间
author:     ZFKY                         # 作者
header-img: img/post-bg-2015.jpg     #这篇文章标题背景图片
catalog: true                         # 是否归档
tags:                                #标签
    - Shadowsocks
---
> 在VPS上搭建Shadowsocks

# 购买VPS

Vultr、DigitalOcean、Virmach、BandwagonHost

# [搭建Shadowsocks](https://www.diycode.cc/topics/738)

运行以下命令：

```
wget --no-check-certificate -O shadowsocks-all.sh https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks-all.sh
chmod +x shadowsocks-all.sh
./shadowsocks-all.sh 2>&1 | tee shadowsocks-all.log
```

选择脚本（Python、R、Go、libev），任选一个：

```
Which Shadowsocks server you'd select:
1.Shadowsocks-Python
2.ShadowsocksR
3.Shadowsocks-Go
4.Shadowsocks-libev
Please enter a number (default 1):
```

笔者选择`Shadowsocks-Go`，输入3......然后，输入密码和端口，笔者直接回车用默认:

```
You choose = Shadowsocks-Go

Please enter password for Shadowsocks-Go
(default password: teddysun.com):

password = teddysun.com

Please enter a port for Shadowsocks-Go [1-65535]
(default port: 8989):

port = 8989


Press any key to start...or Press Ctrl+C to cancel
```

安装成功后，命令行出现：

```
Congratulations, Shadowsocks-Go server install completed!
Your Server IP        :  45.32.73.59
Your Server Port      :  8989
Your Password         :  teddysun.com
Your Encryption Method:  aes-256-cfb

Welcome to visit: https://teddysun.com/486.html
Enjoy it!
```

# [KVM VPS加速](https://www.gaoshilei.com/2017/11/06/SSR/)

安装锐速破解版

```
wget -N --no-check-certificate https://raw.githubusercontent.com/wn789/serverspeeder/master/serverspeeder.sh
```

如果报错 wget 命令找不到，需要安装：

```
yum -y install wget
```

脚本下载完成之后赋权执行：

```
chmod +x serverspeeder.sh
bash serverspeeder.sh
```

如果看到下面这个，证明当前 VPS 系统内核不支持

```
This kernel is not supported. Trying fuzzy matching…
Serverspeeder is not supported on this kernel! View all supported systems and kernels here: https://www.91yun.org/serverspeeder91yun
```

如果你没有看到上面内容，而是看到了

```
[Running Status]
ServerSpeeder is running!
version              3.10.61.0
[License Information]
License              B4C10AE5B485C0CE (valid on current device)
MaxSession           unlimited
MaxTcpAccSession     unlimited
MaxBandwidth(kbps)   unlimited
ExpireDate           2034-12-31
[Connection Information]
TotalFlow            1
NumOfTcpFlows        1
TotalAccTcpFlow      0
TotalActiveTcpFlow   0
[Running Configuration]
accif                eth0       
acc                  1
advacc               1
advinacc             1
wankbps              10000000
waninkbps            10000000
csvmode              0
subnetAcc            0
maxmode              1
pcapEnable           0

```

恭喜你，锐速已经安装完成。