# 概述
1. Linux系统中文件和文件夹，一般有三个权限： 拥有者权限，群组权限，其他人权限
2. 对于root来说，任何文件都有读的权限，但是不一定有写和执行的权限，这个时候就需要你自己更改权限
3. 三种更改权限的方法： chgrp、chown、chmod
```
chgrp: 改变一个文件或者文件夹的群组：chgrp [-R] groupsname filename
chown：改变一个文件或者文件夹的拥有者: chown [-R] user:group filename 
chmod：改变权限
r : 4
w : 2
x : 1
chmod [-R] 777 filename/foldername
u ：user
g : group
o : others
a : all

chmod u+w g-w o+r filename

```
4. 文件的权限和文件夹的权限的区别
```
文件：
r: 读取内容
w: 写入修改内容
x: 执行

文件夹：
r: 读取文件夹的里面的文件名
w: 删除文件，移动文件
x: 进入这个文件夹。如果没有x，w就没有用。

一个开放的目录最少的权限要有r-x

```

# 任务
1. root用户新建一个文件，设置普通用户可写的权限
2. root在普通用户目录下新建一个文件，使用普通用户进行删除
3. root用户新建一个文件，将拥有者和群组修改为普通用户
4. root用户新建一个文件夹，设置为普通用户可读，但是不可进入，不可写
