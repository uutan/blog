title: centOS升级git高版本
date: 2016-10-09 14:41:59
tags: ['git']
---

先升级系统：
```
sudo yum update
```

再安装依赖：
```
sudo yum install curl-devel expat-devel gettext-devel openssl-devel zlib-devel gcc perl-ExtUtils-MakeMaker
```

再安装libiconv:
```
wget http://ftp.gnu.org/pub/gnu/libiconv/libiconv-1.14.tar.gz
tar zxvf libiconv-1.14.tar.gz
cd libiconv-1.14
./configure --prefix=/usr/local/libiconv
make && make install
```

删除旧版本
```
yum remove git
```

下载新版本：
```
wget https://github.com/git/git/archive/v2.3.0.zip
unzip v2.3.0.zip
cd git-2.3.0


# 编译

make prefix=/usr/local/git all
sudo make prefix=/usr/local/git install
```

修改环境变量：
```
sudo vim /etc/profile
export PATH=/usr/local/git/bin:$PATH
source /etc/profile
```
