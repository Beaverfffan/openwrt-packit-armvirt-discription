# openwrt-packit-armvirt-discription
有关armvirt项目的一点点使用介绍。源项目来自flippy ophub 

1.armvirt是什么？
armvirt是openwrt的一种适配格式，你可以理解为arm虚拟机镜像。

2.openwrt-packit是什么？
unifreq/openwrt_packit: Flippy's openwrt packaged source code
https://github.com/unifreq/openwrt_packit
openwrt-packit是flippy制作的打包项目，使用armbian的引导，打包armvirt rootfs文件，形成通用的openwrt适配方式。

3.openwrt-packit适合哪些设备？
主要是s905/s912/s905x2/s905x3/h6/rk3328/rk3568/rk3399/rk3588.
具体设备详见ophub的ophub/amlogic-s9xxx-openwrt与flippy的unifreq/openwrt_packit。

4.如何自行编译armvirt内核？
ophub/amlogic-s9xxx-openwrt: OpenWrt for Amlogic s9xxx tv box. 
https://github.com/ophub/amlogic-s9xxx-openwrt
ophub项目有较为通用的.config,可以复制使用，按照正常的openwrt编译方式编译（区分lede与op master）。https://github.com/ophub/amlogic-s9xxx-openwrt/tree/main/router-config
需要相应添加你自己设备需要添加的特殊外设驱动，config仅仅是保障基础文件系统无问题。

5.从哪里能够获得flippy的引导？
Flippy预编译好的 Arm64 内核 (在 https://t.me/openwrt_flippy 及 https://pan.baidu.com/s/1tY_-l-Se2qGJ0eKl7FZBuQ 提取码：846l)

6.如何初始化打包引导环境？
sudo -E apt-get -qq update
sudo -E apt-get -qq install $(curl -fsSL https://is.gd/depend_ubuntu2204_openwrt)
推荐本地安装宝塔来可视化管理文件，打包路径在根目录opt，而不是ubuntu用户子目录

