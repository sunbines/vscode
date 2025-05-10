# 修复远程主机不满足运行vscode服务器的先决条件.md
自 VS Code 1.99 版本起，官方要求 Linux 系统需搭载 glibc 2.28 或更高版本，这对使用旧版 Linux 的用户造成了挑战。微软提供了一种解决方案，允许用户通过 Remote - SSH 扩展连接到不支持的操作系统，只要提供包含所需库版本的 sysroot。本文介绍了如何在 CentOS 7.9 等系统上构建和部署 sysroot。 步骤概述： 1. 准备 Docker 环境并克隆 vscode-sysroot 仓库。 2. 构建 sysroot 压缩包，使用 Docker 创建镜像并复制生成的压缩包。 3. 上传压缩包到远程服务器，解压到指定目录，并部署 sysroot.sh 脚本。 4. 配置 shell 环境以自动加载 sysroot，并重新登录以使设置生效。 5. 最后，重新打开 VS Code 并连接到远程服务器进行验证。 注意：此方法为技术解决方案，并非官方支持的使用场景。






# 参考资料
 * [修复远程主机不满足运行vscode服务器的先决条件](https://remrin.xlog.app/vscode-remote-fix?locale=zh)