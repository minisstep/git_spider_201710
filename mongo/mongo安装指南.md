# windows下mongodb安装与使用整理


## 启动mongodb_server
```mongo
%启动mongodb_server%
cd C:\Program Files\MongoDB\Server\3.4\bin
mongod.exe --dbpath G:\mongodb\data\db
mongo.exe
pause
```
##  MongoDB安装为windows服务

* 请务必使用“管理员权限”打开cmd命令行，然后输入：
```mongo
mongod.exe  --dbpath "G:\mongodb\data\db" --logpath "G:\mongodb\data\log\db.log" --install --serviceName "mongo" --logappend --directoryperdb

```

## mongo 编辑器


## 参考教程
[Robomongo](https://robomongo.org/)
[windows下mongodb安装与使用整理](http://www.cnblogs.com/lecaf/p/mongodb.html)


MongoDB服务无法启动，发生服务特定错误：100
问题：MongoDB服务无法启动，发生服务特定错误：100
原因：没有正常关闭mongod服务，导致mongod被锁
解决方案：进入db文件夹，删除mongod.lock文件，然后重新启动服务即可