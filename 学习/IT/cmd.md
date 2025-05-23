清楚：CLS

中断：ctrl+c

进入上次d盘所在的目录：d:

显示上次c盘所在的目录：cd c:

安装APK文件（手机打开调试模式）：adb install 文件路径

**一、文件与目录操作**
- **`dir`**  
    列出当前目录下的文件和文件夹（`dir /s` 递归显示子目录内容）。
- **`cd`**  
    切换目录：
    - `cd 目录名`：进入指定目录
    - `cd..`：返回上一级目录
    - `cd \`：回到根目录
- **`md`**  
    创建新文件夹（如 `md "新文件夹名"`）。
- **`rd`**  
    删除空文件夹（`rd 文件夹名 /s` 强制删除非空文件夹）。
- **`del`**  
    删除文件（`del 文件名` 或 `del *.txt` 删除所有 txt 文件）。
- **`ren`**  
    重命名文件或文件夹（如 `ren 旧名 新名`）。
- **`copy`**  
    复制文件（`copy 源文件路径 目标路径`）。
- **`move`**  
    移动文件或重命名文件（`move 源文件路径 目标路径`）。


**二、网络测试**

- **`ping`**  
    测试网络连通性（如 `ping www.baidu.com`）。
    - 参数：`-t` 持续 ping，`-l` 指定数据包大小，`-n` 指定发送次数。
- **`tracert`**  
    追踪数据包路由路径（如 `tracert www.baidu.com`）。
- **`ipconfig`**  
    查看网络配置：
    - `ipconfig`：显示基本 IP 信息
    - `ipconfig /all`：显示详细网络配置（含 MAC 地址、DNS 等）
    - `ipconfig /release` 和 `ipconfig /renew`：释放 / 重新获取 IP 地址。
