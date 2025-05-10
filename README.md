# 概述
用vscode进行ssh连接时，提示`远程主机可能不符合 glibc 和 libstdc++ VSCode 服务器的先决条件`。查了一下发现这个问题主要是由于VSCode在一月份发布的最新版本v1.86中要求远程主机 glibc>=2.28导致。

如下图所示：

![图片](https://raw.githubusercontent.com/sunbines/images/main/工具/67B3C6E19D71C3A64E228153F35664D5.png)

解决方法：

* 回退VSCode版本到1.85.2版本。

* 设置禁止自动更新：`VSCode`设置中搜索：`Update:Mode` ，值改为`none`即可。

查看glic版本：

```bash
# ldd --version
ldd (GNU libc) 2.31
Copyright (C) 2020 Free Software Foundation, Inc.
This is free software; see the source for copying conditions.  There is NO
warranty; not even for MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
Written by Roland McGrath and Ulrich Drepper.
```

# vscode 1.85.2下载网址
各平台的下载链接:
| Download type                        | URL                                                                 |
|-------------------------------------|----------------------------------------------------------------------|
| Windows x64 System installer        | [https://update.code.visualstudio.com/1.85.2/win32-x64/stable](https://update.code.visualstudio.com/1.85.0/win32-x64/stable)         |
| Windows x64 User installer          | [https://update.code.visualstudio.com/1.85.2/win32-x64-user/stable](https://update.code.visualstudio.com/1.85.0/win32-x64-user/stable)    |
| Windows x64 zip                     | [https://update.code.visualstudio.com/1.85.2/win32-x64-archive/stable](https://update.code.visualstudio.com/1.85.0/win32-x64-archive/stable) |
| Windows x64 CLI                     | [https://update.code.visualstudio.com/1.85.2/cli-win32-x64/stable](https://update.code.visualstudio.com/1.85.0/cli-win32-x64/stable)     |
| Windows Arm64 System installer      | [https://update.code.visualstudio.com/1.85.2/win32-arm64/stable](https://update.code.visualstudio.com/1.85.0/win32-arm64/stable)       |
| Windows Arm64 User installer        | [https://update.code.visualstudio.com/1.85.2/win32-arm64-user/stable](https://update.code.visualstudio.com/1.85.0/win32-arm64-user/stable)  |
| Windows Arm64 zip                   | [https://update.code.visualstudio.com/1.85.2/win32-arm64-archive/stable](https://update.code.visualstudio.com/1.85.0/win32-arm64-archive/stable) |
| Windows Arm64 CLI                   | [https://update.code.visualstudio.com/1.85.2/cli-win32-arm64/stable](https://update.code.visualstudio.com/1.85.0/cli-win32-arm64/stable)   |
| macOS Universal                     | [https://update.code.visualstudio.com/1.85.2/darwin-universal/stable](https://update.code.visualstudio.com/1.85.0/darwin-universal/stable)  |
| macOS Intel chip                    | [https://update.code.visualstudio.com/1.85.2/darwin/stable](https://update.code.visualstudio.com/1.85.0/darwin/stable)            |
| macOS Intel chip CLI                | [https://update.code.visualstudio.com/1.85.2/cli-darwin-x64/stable](https://update.code.visualstudio.com/1.85.0/cli-darwin-x64/stable)    |
| macOS Apple silicon                 | [https://update.code.visualstudio.com/1.85.2/darwin-arm64/stable](https://update.code.visualstudio.com/1.85.0/darwin-arm64/stable)      |
| macOS Apple silicon CLI             | [https://update.code.visualstudio.com/1.85.2/cli-darwin-arm64/stable](https://update.code.visualstudio.com/1.85.0/cli-darwin-arm64/stable)  |
| Linux x64                           | [https://update.code.visualstudio.com/1.85.2/linux-x64/stable](https://update.code.visualstudio.com/1.85.0/linux-x64/stable)         |
| Linux x64 debian                    | [https://update.code.visualstudio.com/1.85.2/linux-deb-x64/stable](https://update.code.visualstudio.com/1.85.0/linux-deb-x64/stable)     |
| Linux x64 rpm                       | [https://update.code.visualstudio.com/1.85.2/linux-rpm-x64/stable](https://update.code.visualstudio.com/1.85.0/linux-rpm-x64/stable)     |
| Linux x64 snap                      | [https://update.code.visualstudio.com/1.85.2/linux-snap-x64/stable](https://update.code.visualstudio.com/1.85.0/linux-snap-x64/stable)    |
| Linux x64 CLI                       | [https://update.code.visualstudio.com/1.85.2/cli-linux-x64/stable](https://update.code.visualstudio.com/1.85.0/cli-linux-x64/stable)     |
| Linux Arm32                         | [https://update.code.visualstudio.com/1.85.2/linux-armhf/stable](https://update.code.visualstudio.com/1.85.0/linux-armhf/stable)       |
| Linux Arm32 debian                  | [https://update.code.visualstudio.com/1.85.2/linux-deb-armhf/stable](https://update.code.visualstudio.com/1.85.0/linux-deb-armhf/stable)   |
| Linux Arm32 rpm                     | [https://update.code.visualstudio.com/1.85.2/linux-rpm-armhf/stable](https://update.code.visualstudio.com/1.85.0/linux-rpm-armhf/stable)   |
| Linux Arm32 CLI                     | [https://update.code.visualstudio.com/1.85.2/cli-linux-armhf/stable](https://update.code.visualstudio.com/1.85.0/cli-linux-armhf/stable)   |
| Linux Arm64                         | [https://update.code.visualstudio.com/1.85.2/linux-arm64/stable](https://update.code.visualstudio.com/1.85.0/linux-arm64/stable)       |
| Linux Arm64 debian                  | [https://update.code.visualstudio.com/1.85.2/linux-deb-arm64/stable](https://update.code.visualstudio.com/1.85.0/linux-deb-arm64/stable)   |
| Linux Arm64 rpm                     | [https://update.code.visualstudio.com/1.85.2/linux-rpm-arm64/stable](https://update.code.visualstudio.com/1.85.0/linux-rpm-arm64/stable)   |
| Linux Arm64 CLI                     | [https://update.code.visualstudio.com/1.85.2/cli-linux-arm64/stable](https://update.code.visualstudio.com/1.85.0/cli-linux-arm64/stable)   |


# 参考资料
* [远程主机可能不符合glibc和libstdc++ VS Code服务器的先决条件](https://blog.csdn.net/qq_39435411/article/details/136063652)
* [Visual Studio Code™ portable](https://portapps.io/app/vscode-portable/)
* [2025 年 VSCode 插件离线下载攻略：官方渠道一键获取](https://zhuanlan.zhihu.com/p/26003070992)