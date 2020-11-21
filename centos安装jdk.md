安装之前先检查一下系统有没有自带`open-jdk`

命令：

```
rpm -qa |grep javarpm -qa |grep jdkrpm -qa |grep gcj
```

如果没有输入信息表示没有安装。

如果安装可以使用`rpm -qa | grep java | xargs rpm -e --nodeps `批量卸载所有带有Java的文件 这句命令的关键字是java

首先检索包含java的列表

```
yum list java*
```

检索1.8的列表

```
yum list java-1.8* 
```

安装1.8.0的所有文件

```
yum install java-1.8.0-openjdk* -y
```

使用命令检查是否安装成功

```
java -version
```