清楚：CLS

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

**三、系统管理与服务**
#### 1. **进程管理**

- **`tasklist`**  
    显示当前运行的进程（`tasklist /svc` 显示进程对应的服务）。
- **`taskkill`**  
    终止进程：
    - `taskkill /f /im 进程名.exe`：强制终止指定进程
    - `taskkill /pid 进程ID`：通过 PID 终止进程

#### 2. **服务管理**

- **`net start`**  
    启动服务（如 `net start "Windows Update"`）。
- **`net stop`**  
    停止服务（如 `net stop "Windows Update"`）。
- **`sc`**  
    服务控制工具（如 `sc query 服务名` 查看服务状态）。

#### 3. **用户与权限**

- **`net user`**  
    管理用户账户：
    - `net user`：列出所有用户
    - `net user 用户名`：查看用户详细信息
    - `net user 用户名 新密码 /add`：创建新用户
    - `net user 用户名 /del`：删除用户
- **`net localgroup`**  
    管理用户组（如 `net localgroup Administrators 用户名 /add` 将用户加入管理员组）。

**四、系统工具与调试**

- **`notepad`**  
    打开记事本程序。
- **`calc`**  
    打开计算器。
- **`mspaint`**  
    打开画图工具。
- **`regedit`**  
    打开注册表编辑器（需谨慎操作，错误修改可能导致系统故障）。
- **`msconfig`**  
    打开系统配置工具（用于管理启动项、服务等）。
- **`eventvwr`**  
    打开事件查看器（查看系统日志）。

**五、其他实用命令**

- **`shutdown`**  
    关机 / 重启：
    - `shutdown -s -t 60`：60 秒后关机
    - `shutdown -r -t 0`：立即重启
    - `shutdown -a`：取消关机计划
- **`sfc`**  
    系统文件检查工具（`sfc /scannow` 扫描并修复系统文件错误）。
- **`dism`**  
    系统映像修复工具（如 `dism /online /cleanup-image /restorehealth`）。
- **`color`**  
    修改命令提示符窗口颜色（如 `color 0a` 设置黑底绿字）。
- **`help`**  
    查看命令帮助（如 `help dir` 查看 `dir` 命令的用法）。

### **技巧与说明**

1. **命令补全**：按 **Tab 键** 可自动补全目录或文件名（需开启命令提示符的 “历史记录” 功能）。
2. **管道与重定向**：
    - `|`：管道符，将前一个命令的输出作为后一个命令的输入（如 `dir | find "txt"` 筛选包含 “txt” 的文件）。
    - `>`：重定向输出到文件（如 `dir > list.txt` 将目录列表保存到 list.txt）。
3. **快捷键**：
    - `Ctrl + C`：终止当前命令执行
    - `Ctrl + V`：在命令提示符中粘贴文本（`Ctrl + 右键` 也可粘贴）
    - `Win + R`：快速打开 “运行” 窗口，输入命令后按回车执行。
