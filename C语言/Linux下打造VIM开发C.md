# 一步步将VIM打造成C/C++（IDE）

使用apt-get遇到的问题：

```shell
yimiao@yimiao-virtual-machine:/etc/vim$ sudo apt-get install vim-scripts
E: 无法获得锁 /var/lib/dpkg/lock - open (11: 资源暂时不可用)
E: 无法锁定管理目录(/var/lib/dpkg/)，是否有其他进程正占用它？
```

解决：
```
sudo rm /var/cache/apt/archives/lock
sudo rm /var/lib/dpkg/lock
sudo dpkg --configure -a
dpkg：错误：正在解析文件 '/var/lib/dpkg/updates/0012' 第 0 行附近:
在字段名 #padding 中发现换行符
sudo rm /var/lib/dpkg/updates/*
sudo apt-get update
sudo apt-get upgrade
```

## vim基本配置
```
syntax on " 语法高亮
```

## Linux下eclipse开发C/C++
```
解压eclipse进入目录
ln -s /usr/local/jdk/jre/ jre
```

```
  配置eclipse桌面快捷方式
  1 [Desktop Entry]
  2 Encoding=UTF-8
  3 Name=Eclipse
  4 Comment=client
  5 Exec=/usr/local/eclipse/eclipse
  6 Icon=/usr/local/eclipse/icon.xpm
  7 Terminal=false
  8 Type=Application
  9 StartupNotify=true
 10 Categories=Application;Development;

```
