# computer-network

## 课程

【【网络】半小时看懂<计算机网络>】https://www.bilibili.com/video/BV124411k7uV?vd_source=7252f507b661da5c766c13355b3350ee

## ip地址
IP地址 = 网络地址 + 主机地址(又称：主机号和网络号组成)


我们要找到指定的IP地址，只要先找到指定的网络地址，然后再该网络内找到对应的主机地址即可。

IP地址是一个 4 * 8bit（1字节）由 0/1 组成的数字串（IP4协议）

以文章开通 win7 截图中 的 IP地址 192.168.1.168, 子网掩码 255.255.255.0(下文有详解) 为例, 这个地址中包含了很多含义:

192.168.100.168（IP地址） = 192.168.1.0 (网络地址) + 0.0.0.168（主机地址）


## 子网掩码

长度 为 4 * 8bit（1字节），由 连续的1 以及 连续的0 两部分组成，

例如：11111111.11111111.11111111.00000000，对应十进制：255.255.255.0

假设，局域网中 计算机A 的IP地址为 192.168.1.1，子网掩码为 255.255.255.0， 如下图所示：

img

网络地址: IP 地址中被 连续的1 遮住的部分，即 11000000.10101000.00000001.00000000, 对应的网络地址：192.168.1.0

主机地址: IP 地址中被 连续的0 遮住的部分，即 00000000.00000000.00000000.00000001, 对应的网络地址：0.0.0.1

排除 该网络 两个特殊地址：

广播地址：192.168.1.255　　（主机号全为11111111）（广播机制及类型见：http://baike.baidu.com/view/473043.htm）

网络地址：192.168.1.0 　　　（主机号全为00000000）

该子网最大的主机数：2的8次方 256 - 2

其他信息：

A类地址来说，默认的子网掩码是255.0.0.0；对于B类地址来说默认的子网掩码是255.255.0.0；对于C类地址来说默认的子网掩码是255.255.255.0
