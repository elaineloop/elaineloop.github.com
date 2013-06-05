---
layout: post
title: "mysql previleges instruction"
description: ""
category: mysql
tags: [previleges]
---
{% include JB/setup %}
## 普通用户权限描述 ##
   - SELECT允许用户从表中选择行
   - INSERT       允许用户在表中插入新行
   - UPDATE       允许用户修改现存表里行中的值
   - DELETE       允许用户删除现存表的行
   - INDEX        允许用户创建和拖动特定表索引
   - ALTER        允许用户改变表的结构
   - CREATE       允许用户创建数据库或表
   - DROP         允许用户删除拖动数据库或表
## 管理员权限描述 ##
   - CREATE TEMPORARY TABLES      允许管理员在CREATE TABLE 语句中使用TEMPORARY 关键字
   - FILE                         允许将数据从文件读入表，或者从表读入文件
   - LOCK TABLES                  允许使用LOCK TABLES 语句
   - PROCESS                      允许管理员查看属于所有用户的服务器进程
   - EXCUTE                       可以执行程序
   - RELOAD                       允许重新载入，清空授权，主机、日志和表格，如flush
   - REPLICATION CLIENT           允许在Master主机和Slave主机上使用 SHOW STATUS
   - REPLICATION SLAVE            允许从主机连接到主服务器上
   - SHOW DATABASES               允许使用SHOW DATABASES语句查看数据库列表，否则只能看到自己的数据库
   - SHUTDOWN                     允许管理员关闭Mysql服务器
   - SUPER                        允许管理员关闭任何用户线程
## 特别权限描述 ##
   - ALL(ALL PREVILEGES)  授予所有权限
   - USAGE                不授予权限(创建个用户，只允许登录，但不允许其他操作)
