# Ubuntu 22.04 PWN 预装环境虚拟机

> 一份开箱即用的 Ubuntu 22.04 虚拟机，已按 [博客园《Ubuntu22.04搭建PWN环境》](https://www.cnblogs.com/LY613313/p/16180458.html) 教程预装好 PWN 调试与利用所需的全部工具，专为网安实战 / CTF 中的 PWN 方向学习使用。




## 1. 网盘下载

虚拟机镜像已上传至网盘，请使用以下链接下载：


通过网盘分享的文件：ubuntu22.04
链接: https://pan.baidu.com/s/1zqJ6zh37sk6GthjQJTepdA 提取码: niqc 
--来自百度网盘超级会员v2的分享

---

## 2. 项目简介

- **仓库用途**：提供一份预装好 PWN 工具链的 Ubuntu 22.04 虚拟机镜像下载入口，供网安实战学习者直接使用，避免重复搭建环境
- **系统版本**：Ubuntu 22.04 LTS
- **参考教程**：[LY613313《Ubuntu22.04搭建PWN环境》](https://www.cnblogs.com/LY613313/p/16180458.html)

---

## 3. 虚拟机配置

| 项目 | 配置 |
| --- | --- |
| 操作系统 | Ubuntu 22.04 LTS（默认安装，无额外桌面美化） |
| 用户名 密码 | `ctf` `ctf` |
| 虚拟化软件 |  VMware Workstation  |

---


## 4. 已安装工具清单

工具均与博客原文保持一致，全部安装在当前用户下。

为了方便编写代码，同时安装了Microsoft VS Code


### GDB 插件切换方式

`~/.gdbinit` 已配置好三个插件的 `source` 入口，默认启用 pwndbg，其余两个注释掉。如需切换：

```bash
sudo vim ~/.gdbinit
```

```text
# 默认启用 pwndbg：
source /home/<用户名>/桌面/pwn_tool/pwndbg/gdbinit.py

# 切换为 peda（取消注释下面这行，并注释上面那行）：
# source /home/<用户名>/桌面/pwn_tool/peda/peda.py

# 切换为 gef（取消注释下面这行，并注释其他两行）：
# source /home/<用户名>/桌面/pwn_tool/gef/gef.py
```

保存后再次执行 `gdb` 即可生效。

---

tips：虚拟机常拍快照，可以避免一些不必要的问题