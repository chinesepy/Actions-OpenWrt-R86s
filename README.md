 [介绍](https://p3terx.com/archives/build-openwrt-with-github-actions.html)

# Actions-OpenWrt

A template for building OpenWrt with GitHub Actions

## Tips

- 自用openwrt固件for R86S 2.5G网卡版（脚本删除了编译后上传网盘，修改了set-output，添加了kenzok8的两个源，未修改默认ip；config文件是自己瞎改的，参考了 [OpenWrt-Rpi](https://github.com/SuLingGG/OpenWrt-Rpi)的内容，删除了无线相关、usb相关、除了翻墙外的VPN、samba、netdata、磁盘休眠、内网穿透、以及下载工具，添加了Socat、迅雷快鸟、wol、kms以及IPTV用的udpxy和omcproxy，主题为argonne带自定义配置）


## 软件源
- 配置注释掉 # option check_signature
- 注释掉自带软件源里头的kenzok和small的两个无效源
- 自定义软件源
- src/gz openwrt_core https://openwrt.cc/snapshots/targets/x86/64/packages
- src/gz openwrt_base https://openwrt.cc/snapshots/packages/x86_64/base
- src/gz openwrt_luci https://openwrt.cc/snapshots/packages/x86_64/luci
- src/gz openwrt_packages https://openwrt.cc/snapshots/packages/x86_64/packages
- src/gz openwrt_routing https://openwrt.cc/snapshots/packages/x86_64/routing
- src/gz openwrt_telephony https://openwrt.cc/snapshots/packages/x86_64/telephony

## Usage

- Click the [Use this template](https://github.com/P3TERX/Actions-OpenWrt/generate) button to create a new repository.
- Generate `.config` files using [Lean's OpenWrt](https://github.com/coolsnowwolf/lede) source code. ( You can change it through environment variables in the workflow file. )
- Push `.config` file to the GitHub repository.
- Select `Build OpenWrt` on the Actions page.
- Click the `Run workflow` button.
- When the build is complete, click the `Artifacts` button in the upper right corner of the Actions page to download the binaries.

## Credits

- [Microsoft Azure](https://azure.microsoft.com)
- [GitHub Actions](https://github.com/features/actions)
- [OpenWrt](https://github.com/openwrt/openwrt)
- [Lean's OpenWrt](https://github.com/coolsnowwolf/lede)
- [tmate](https://github.com/tmate-io/tmate)
- [mxschmitt/action-tmate](https://github.com/mxschmitt/action-tmate)
- [csexton/debugger-action](https://github.com/csexton/debugger-action)
- [Cowtransfer](https://cowtransfer.com)
- [WeTransfer](https://wetransfer.com/)
- [Mikubill/transfer](https://github.com/Mikubill/transfer)
- [softprops/action-gh-release](https://github.com/softprops/action-gh-release)
- [ActionsRML/delete-workflow-runs](https://github.com/ActionsRML/delete-workflow-runs)
- [dev-drprasad/delete-older-releases](https://github.com/dev-drprasad/delete-older-releases)
- [peter-evans/repository-dispatch](https://github.com/peter-evans/repository-dispatch)

## License

[MIT](https://github.com/P3TERX/Actions-OpenWrt/blob/main/LICENSE) © [**P3TERX**](https://p3terx.com)
