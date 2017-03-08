---
title: PLSQL Developer连接Oracle11g 64位数据库配置详解
---
最近换了台64bit的电脑，所以oracle数据库也跟着换成了64bit的，不过问题也随之产生，由于plsql developer暂时没有64bit版本的，所以无法连接到64bit的oracle上，经过一番折腾，终于成功连接到数据库上，现记录下配置过程，以便查看。

## 步骤

### 1.下载instantclient-basic-win32-11.2.0.1.0
oracle官网下载地址:http://www.oracle.com/technetwork/topics/winsoft-085727.html 
<br/>
下载地址2：http://download.csdn.net/detail/czw2010/5732241

### 2. 解压instantclient-basic-win32-11.2.0.1.0
解压instantclient-basic-win32-11.2.0.1.0并放置在oracle安装目录的product下(放置位置无强制要求，可随意放置)
![](/images/20170308/1.png)<br/>

### 3. 拷贝E:\app\Administrator\product\11.2.0\dbhome_1\NETWORK文件夹到instantclient_11_2下。

### 4. 打开PLSQL Developer，选择Tools -> perference -> Connection，配置其中的Oracle Home和OCI Library项，如下图所示：
![](/images/20170308/2.png)<br/>
其中, Oracle Home：E:\app\Administrator\product\instantclient_11_2
OCI Library：E:\app\Administrator\product\instantclient_11_2\oci.dll


