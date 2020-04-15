# 借助 GitHub Actions 云编译 OpenWrt x86_64

`Github Actions` 是 GitHub 推出的持续集成服务，它提供了配置非常不错的虚拟服务器环境（E5 2vCPU/7G RAM），基于它可以进行构建、测试、打包、部署项目。

## 项目介绍

- 本项目直接调用大雕[Lean's OpenWrt](https://github.com/coolsnowwolf/lede)、[Lienol's OpenWrt](https://github.com/Lienol/openwrt-package)开源仓库源码，保证纯净

- 借助`Github Actions`自动生成openwrt固件，感谢大雕[KFERMercer](https://github.com/KFERMercer/OpenWrt-CI)、[P3TERX](https://github.com/P3TERX/Actions-OpenWrt)、[esir](https://github.com/esirplayground/AutoBuild-OpenWrt)

- 定制化编译---必须熟悉整个openwrt编译过程，修改目录下的`x86_64.config` `Build_OP_x86_64.yml`文件即可定制

- 无需搭建编译环境生成.config文件---可选择在线make menuconfig生成配置文件，感谢大雕[P3TERX](https://github.com/P3TERX/debugger-action)

- `fork`此项目后，点击顶部的`star`即可开始编译`openwrt`固件，真正的一键开始编译

- 本项目插件来源的源码仓库：[Lean's OpenWrt](https://github.com/coolsnowwolf/lede)、[Lienol's OpenWrt](https://github.com/Lienol/openwrt-package)、[Adguard Home插件](https://github.com/rufengsuixing/luci-app-adguardhome)、[OpenClash插件](https://github.com/vernesong/OpenClash)、[Clash插件](https://github.com/frainzy1477/luci-app-clash)、[KoolProxyR plus+插件](https://github.com/jefferymvp/luci-app-koolproxyR)

- `fork`此项目后，默认每月1、12、23号自动编译新固件，(可在`Build_OP_x86_64.yml`文件中的`schedule` 和 `- cron`前面添加`# `取消此功能)---进入`Actions`标签页后，选择已完成的`workflows`后，在右方的`Artifacts`即可看到编译的固件

## 操作步骤

- 注册[GitHub](https://github.com/join)账号

- `Fork`此仓库源码 [GitHub repository](https://github.com/superstarfly/AutoBuild-OpenWrt-E)

- 定制化固件---编辑`x86_64.config` `Build_OP_x86_64.yml`文件即可定制

- 开始编译，可在`Actions`标签页进行查看--1）点击顶部`star`即可开始编译；2）也可进入`Build_OP_x86_64.yml`文件取消`push` `branches` `maser`前面`#`开始编译； 3）其他解锁编译由你来发现

- 大功告成，下载固件---进入`Actions`标签页后，选择已完成的`workflows`后，在右方的`Artifacts`即可看到编译生成的固件

- OpenWrt默认lan IP： `192.168.5.1`, 用户名 `root`，密码 `password`

## 固件包含的常用插件(多功能Q版)

- 主要功能： `Ssr Plus+` `Passwall`  `Openclash`  `clash`  `Adguard Home` `多线多拨` `负载均衡`

- 其他功能： `KoolProxyR plus+` `广告屏蔽大师plus+` `aria2` `transmission` `解锁网易云灰色歌曲` `动态DNS` `Frp内网穿透` `frps服务端` `Kms服务器` `Openvpn` `Baidupcs web` `Pptp VPN` `IPSec VPN` `SoftEther VPN` `ssr-server` `v2ray-server` `openvpn-server`

## 固件插件截图(多功能Q版)

![image](https://github.com/superstarfly/autobuild-openwrt/raw/master/imgfiles/openwrt-QQ.jpg)
