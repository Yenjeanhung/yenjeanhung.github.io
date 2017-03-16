---
title: oracle导出命令exp和导入命令imp的使用
---
本方介绍使用oracle的exp命令导出数据和imp命令导入数据的具体操作

## 导出命令EXP

  exp有三种主要的方式（完全、用户、表）

   1. 完全模式：

	``` 
	EXP SYSTEM/MANAGER BUFFER=64000 FILE=C:\FULL.DMP FULL=Y
	```

	---
	如果要执行完全导出，必须具有特殊的权限      

   2. 用户模式：
	
	``` 
	EXP SONIC/SONIC    BUFFER=64000 FILE=C:\SONIC.DMP OWNER=SONIC
	```

	---
    这样用户SONIC的所有对象被输出到文件中。

   3. 表模式：

   	``` 
	EXP SONIC/SONIC    BUFFER=64000 FILE=C:\SONIC.DMP OWNER=SONIC TABLES=(SONIC)
	```

	---
	这样用户SONIC的表SONIC就被导出 

## 导入命令IMP

 imp有三种模式（完全、用户、表）

1. 完全模式：

	``` 
	IMP SYSTEM/MANAGER BUFFER=64000 FILE=C:\FULL.DMP FULL=Y
	```
 	
	---
	

2. 用户模式：

	``` 
	IMP SONIC/SONIC    BUFFER=64000 FILE=C:\SONIC.DMP FROMUSER=SONIC TOUSER=SONIC
	```
	
	---
   这样用户SONIC的所有对象被导入到文件中。必须指定FROMUSER、TOUSER参数，这样才能导入数据。

3. 表模式：

	``` 
	EXP SONIC/SONIC  BUFFER=64000 FILE=C:\SONIC.DMP OWNER=SONIC TABLES=(SONIC)
	```

	---
   这样用户SONIC的表SONIC就被导入。



参考: [oracle中exp,imp的使用详解](http://www.cnblogs.com/yugen/archive/2010/07/25/1784763.html)
