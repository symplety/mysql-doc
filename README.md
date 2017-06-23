# mysql-doc
数据库设计

1. 
```linux
 mysql -u root -p
```
   通过使用该命令进入数据库，以检查数据库是否安装成功。
  
2.
```mysql
 show databases; 
```
   该命令可以查看当前有那些数据库（注意其中database**s**是复数形式）。
3.
```mysql
 create database stu;
 ```
   该命令用来创建名字为**stu**的数据库。

4.
```mysql
 use stu；
```
   该命令用来改变当前所在的数据库为**stu**。
  
5.
```mysql
 create table <表名>
 （<属性名1> <数据类型> [not null],
   <属性名2> <数据类型> [not null],
   ...
   [primary key('某属性名'),]
   [foreign key('某属性名') references <表名>('某属性名')]
   ）；
   ```
     该语句块用来创建 **school、information、course、score**（学院信息、学生信息、课程信息、成绩）三个表，其中主码、外码可以根据实际情况来设置。
 
 ## school表的属性信息
 
   属性名 |数据类型 | 数据长度 |是否为主码 |是否能为空
   -------|-------|---------|---------|---------
   学院编号（scid）|char|5|是|否
   学院名称（scname）|char |50|否|是
 
  
## information表的属性信息
  属性名 | 数据类型 | 数据长度 | 是否为主码 | 是否为外码| 是否能为空  
  ------|---------|---------|-----------|--------|-------- 
  学生编号（id）|int| 12 |是|否|否
  学院编号（scid) | char |5|否|是|否
  学生姓名（sname）|char |20|否|否|是
  学生年龄（age）|int|-|否|否|是
  性别（sex）|char|10|否|否|是
  年级（grade）|char|否|否|是
  
  ## course表的属性信息
  
  属性名 | 数据类型 | 数据长度 | 是否为主码 | 是否为外码| 是否能为空  
  ------|---------|---------|-----------|--------|-------- 
  课程编号（cid）|int| 20 |是|否|否
  课程名字（cname）|char|20|否|否|否
  学院编号（scid) | char |5|否|是|否
  
  
  ## score表的属性信息
  属性名 | 数据类型 | 数据长度 | 是否为主码 | 是否为外码| 是否能为空
  ------|---------|---------|-----------|--------|--------
  学生编号（id）|int| 12 |是|是|否
  课程编号（cid) | char |20 |是|是|否
  成绩（score）|int|-|否|否|是
  
  
  ## 技术文档
* [第一天，linux配置](第一天.md)
* [第二天，linux操作及工具使用](第二天.md)
* [第三天，github使用](第三天.md)
* [第四天，数据库配置](第四天.md)
* [第五天，数据库使用](第五天.md)
* [第六天，atom](第六天.md)

