## MYSQL数据库基本操作
* 00.创建/删除/选择数据库
```mysql
CREATE DATABASE IF NOT EXISTS tb default character set utf8 COLLATE utf8_general_ci;
DROP DATABASE IF EXISTS td;
USE DATABASE td; 
```
* 01.查看/修改数据库默认编码
```mysql
show variables like 'character_set_%'
alter database td CHARACTER SET gb2312;
```
* 02.建表
```mysql
create table t(
`id` INT NOT NULL AUTO_INCREMENT,
`name` VARCHAR(100) NOT NULL,
`ct` VARCHAR(100) NOT NULL, 
`updated_at` DATE NOT NULL,
`bt` INT NOT NULL, 
PRIMARY KEY (`id`)
);
```
* 03.查看/删除表
```mysql
show tables;
drop table t;
```
* 04.显示表结构
```mysql
desc/describe 表
show columns from 表
```
* 05.往表里插入数据
```mysql
INSERT INTO `t` (`id`, `name`, `ct`, `updated_at`, `bt`) VALUES ('2', 'bbb', 'bbb', '2017-03-21', '222');
INSERT INTO `t` (`id`, `name`, `ct`, `updated_at`, `bt`) VALUES ('3', 'ccc', 'ccc', now(), '333');
INSERT INTO `t` (`id`, `name`, `ct`, `updated_at`, `bt`) VALUES ('4', 'ddd', 'ddd', now(), '444'),('5', 'eee', 'eee', now(), '555');
```
* 06.查询
```mysql
select id,name from t;
```
* 07.创建用户并赋权:
```mysql
CREATE USER 'username'@'host' IDENTIFIED BY 'password';
```
* 08.单独赋权
```mysql
GRANT ALL PRIVILEGES ON *.* TO 'root'@'%' IDENTIFIED BY '123456' WITH GRANT OPTION;
FLUSH PRIVILEGES;
```
* 09.收回权限
```mysql
#收回权限(不包含赋权权限)
REVOKE ALL PRIVILEGES ON *.* FROM cacti;
REVOKE ALL PRIVILEGES ON cacti.* FROM cacti;
#收回赋权权限
REVOKE GRANT OPTION ON *.* FROM cacti;
FLUSH PRIVILEGES;
```
