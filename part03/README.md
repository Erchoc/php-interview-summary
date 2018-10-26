## part03. Linux基础考察点

1. 写出尽可能多的 Linux 命令。
> 考点：Linux常用命令，系统定时任务，vi/vim编辑器，shell基础。

2. 如何实现每天0点重新启动服务器?
> crontab -e
> 0 0 * * * reboot

3. 如何实现每个月的4号,每个礼拜的礼拜一到礼拜四的下午3点30分记录时间
> 30 15 4 * 1-4 date +'\%Y=\%m-\%d \%H:\%m' >> ~/cron/date.log

4. 如何实现每两个小时执行一个python脚本?
> 0 */2 * * * * root run-parts ~/cron/cron.py

5. 每天下午4点、5点、6点的5 min、15 min、25 min、35 min、45 min、55 min时执行命令。 
> 5，15，25，35，45，55 16，17，18 * * * echo 'OK' >> ~/cron/multi.log

#### Linux 常用命令(以下每个命令和常用参数的用法都要理解)
- 系统安全: sudo, su, chmod, setfacl
- 进程管理: w, top, ps, kill, pkill, pstree, killall
- 用户管理: id, usermod, useradd, groupadd, userdel 
- 文件系统: mount, umount, fsck, df, du 
- 系统关机和重启: shutdown, reboot 
- 网络应用: curl, wget, mail, elinks 
- 网络测试: ping, tcping, netstat, host 
- 网络配置: hostname, ifconfig
- 常用工具: ssh, screen, clear, who, date 
- 软件包管理: yum, rpm, apt-get, apk 
- 文件查找和比较: locate, find 
- 文件内容查看: cat, head, tail, less, more 
- 文件处理: touch, unlink, rename, ln 
- 目录操作: cd, mv, rm, pwd, tree, cp, ls
- 文件权限属性: setfacl, chmod, chown, chgrp 
- 压缩解压: bzip2/bunzip2, gzip/gunzip, zip/unzip, tar 
- 文件传输: ftp, scp, lrzsz 

#### Linux 系统定时任务
- crontab -e
> 分时日月周

- at
> 某个具体时间点

#### vi/vim编辑器
- 一般模式: 删除, 复制, 粘贴
- 编辑模式: 写代码
- 命令行模式: 查找
- vim的视图模式: v/V, y, d, Ctrl+V

- 一般模式切换到编辑模式: i/I, o/O, a/A, r/R
- 编辑模式切换到一般模式: ESC
- 一般模式切换到命令行模式: :, /, ?

- 移动光标: Ctrl+F, Ctrl+B, 0, G, gg, N+Enter, Home, $, End
- 查找替换: /xxx, ?xxx, :xxx
- 删除复制粘贴: x/X, p/P, dd/ndd, yy/nyy, . , Ctrl+R
- 保存退出: w, q, wq, !

- 命令行模式配置: :setnu, :setnonu

#### shell基础
- 脚本执行方式一(赋予权限后执行): chomd +x xxx.sh, ./xxx.sh
- 脚本执行方式二(调用相应解释器): bash, csh, ash, bsh, ksh
- 脚本执行方式二(使用source命令): source xxx.sh 

- 文件编写前: 开头使用 #! 指定脚本的解释器,如: #!/bin/sh
- shell语言: 常量变量, 流程控制语句, 函数定义和调用

#### 解题方法
> PHP 面试不会问太底层的 Linux 知识, 重点还是放在 PHP 语言和数据库层面。

