title: git签项目到一个非空的目录中
date: 2016-01-04 01:11:12
author: me
---


当我们往一个非空的目录下 clone git 项目，就会提示错误信息。
```bash
fatal: destination path '.' already exists and is not an empty directory.
```

解决方法：
```bash
# 1. 先签到一个空子目录下
git clone --no-checkout https://github.com/uutan/uutan.github.com.git tmp
# 2. 将 tmp 目录下的 .git 目录移到当前目录 (注意点)
mv tmp/.git .
# 3. 删除第一步的子目录
rmdir tmp
# 4. 重置git
git reset --hard HEAD
```

该操作经常会碰到，记录留存。
