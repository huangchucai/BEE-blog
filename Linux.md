# Linux
### 基本知识

1. Linux中一些都是文件
  * 标准输出
  * 标准输入
  * 标准错误
### Linux文件系统
Linux使用的是树形结构管理文件，遵守一定的惯例
1. /  - 根目录
2. /home - 用户目录
3. /var - 经常变化的文件，例如：日志
4. /usr - 用户程序，库
5. /bin - 可执行文件
6. /boot - 引导系统启动
7. /tmp - 临时文件
8. /lib,/lib64 - 系统库文件
### 修改文件的权限

Linux中用

> **Linux 把文件或目录权限的控制分别以读取、写入、执行三种情况区分（权限设置）**  
> `r`  :   读取权限， 数字代号为“4”
> `w`  :   写入权限， 数字代号为“2”
> `x`  :   执行或切换权限，数字代表为“1”
> `-`  :   不具任何权限，数字代表为“0”
> `S`  :   特殊功能说明：变更文件或目录的权限。
> **Liunx把用户也分为三种(权限范围)**  
> `u`  User:  即文件或目录的拥有者
> `g`  Group: 即文件或目录的所属群组
> `o`  Other:  除了文件或目录拥有者或所属群组之外，其他用户皆属于这个范围
> `a`  All:  即全部的用户，包含拥有者，所属群组以及其他用户
> ![](chmod.gif)
> **语法**  
```javascript
chmod (选项) （参数）
// 用法
chmod <权限范围>+<权限设置> 文件 开启权限范围的文件或目录的该选项权限设置
chmod <权限范围>-<权限设置> 文件 关闭权限范围的文件或目录的该选项权限设置

// 执行
chmod u+x test.lua
-rwxr-xr-- 1 root root 169 9月   5 11:28 download_geoip.sh*
-rw-r--r-- 1 root root 360 9月   5 11:30 md5url.sh
-rwx------ 1 root root  34 9月  11 19:59 test.lua*
```

### 终端、SHELL、管道
1. 进程和程序的关系