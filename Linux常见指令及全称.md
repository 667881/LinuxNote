# Linux常见指令及全称

pwd:print working directory，打印当前工作目录







## 用户管理

id xx：查询用户信息

useradd xx：添加用户

useradd -g 用户组 用户名：添加用户并指定组

groupadd xx：添加组

usermod -g 用户组 用户名：将用户切换到另一个组

userdel xx：删除用户，保留其home目录

userdel -r xx：删除用户，连带home目录

su - xx：switch user，切换用户

groupdel xx：删除组

passwd xx：给用户设置密码



## vim常用快捷键

拷贝当前行	yy，拷贝当前行向下的5行	5yy，并粘贴(输入p)

删除当前行	dd，删除当前行向下的5行	5dd





## 实用指令

man xx：帮助指令

help xx：帮助指令



### 文件目录类

ls：显示目录下的文件和目录	-a：显示所有文件和目录，包括隐藏的	-l：以列的方式展现

cd：change directory，切换到指定目录	~：回到家目录	..：回到上级目录

mkdir：用于创建目录	-p：创建多级目录

rmidr：删除空目录

删除非空目录则需要使用rm -rf

rm xx：移除文件或目录	-r：递归删除整个文件夹	-f：强制删除不提示

touch xx：创建一个空文件

cp source dest：拷贝文件到指定目录	-r：递归复制整个文件夹

\cp -r source dest：复制时不提示，强制进行覆盖

mv movefile targerFolder：移动文件与目录或重命名

cat xx：查看文件内容	-n：显示行号

**cat只能浏览文件而不能修改文件，为了浏览方便，一边会带上	管道命令|more**

more指令是一个基于VI编辑器的文本过滤器，它以全屏幕的方式按页显示文本文件的内容。space：翻页

enter：下一行	q：退出	Ctrl+F：向下滚动一屏	Ctrl+B：返回上一屏	=：输出当前行号

less xx：用来分屏查看文件内容，功能与more类似但是更加强大	/字串：可以查找字串，n向下查找，N向上查找

echo xx：输出内容到控制台

head xx：用于显示文件的开头部分内容，默认显示前10行

tail xx：用于显示文件的尾部部分内容，默认显示10行	-f：实时追踪文件变化

\>指令和\>>指令：\>输出重定向，\>>追加

基本语法：ls -l > 文件(列表的内容写入文件a.txt中)	ls -al >> 文件(列表的内容追加到文件aa.txt的末尾)

ln -s [原文件或目录] [软链接名]：给原文件创建一个软连接

history：查看已经执行过的历史命令，也可以执行历史命令	history n：展示最近使用的n条指令	!n：执行历史编号为n的指令



### 时间日期类

date：显示当前时间

date -s  字符串时间：设置日期

cal [选项]：当月日历	选项写年份则展示整年日历



### 探索查找类

find [搜索范围] [选项]：查找文件	-name：按名称查找	-user：查找属于指定用户所有文件	-size：按指定文件大小查找

locate 搜索文件：快速定位文件路径	由于是基于数据库进行查询，第一次运行前必须用updatedb创建数据库

which 指令：查找某个指令的路径

grep 过滤查找，管道符	"|"	表示将前一个命令的处理结果输出传递给后面的命令处理

grep [选项] 查找内容 源文件	-n：显示行号	-i：忽略字母大小写



### 压缩和解压类

gzip 文件：压缩文件为*.gz

gunzip 文件：解压缩文件