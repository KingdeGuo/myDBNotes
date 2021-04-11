[toc]

# 使用MySQL

## 登录

- `mysql -u root -p` 回车之后输入密码即可登录

## 数据库模式

- `show databases;`显示所有数据库

- `use databasename;`选择使用的数据库

- `show tables;`列出所有表

- `show create table tablename;`显示建表语句

  ![image-20210411093224045](https://raw.githubusercontent.com/KingdeGuo/myPictureBed/main/img_upload202104/11/093226-331491.png)

- `show columns from tablename;`用来显示表列

  ![image-20210411093407181](C:\Users\asus\AppData\Roaming\Typora\typora-user-images\image-20210411093407181.png)

- `describe table`是`show columns from tablename`的简写行式。

## 关于show的其他一些用法

- `show status;`用于显示广泛的服务器状态信息。

  ![image-20210411094246262](https://raw.githubusercontent.com/KingdeGuo/myPictureBed/main/img_upload202104/11/094250-979027.png)

- `show create database databasename;`用于显示建立数据库的语句

  ![image-20210411094325502](https://raw.githubusercontent.com/KingdeGuo/myPictureBed/main/img_upload202104/11/094327-277042.png)

- `show grants`用于显示授予用户的安全权限

  ![image-20210411094349541](C:\Users\asus\AppData\Roaming\Typora\typora-user-images\image-20210411094349541.png)

- `show errors`或者`show warnings`用来显示服务器的错误或者警告信息。

  ![image-20210411094418914](C:\Users\asus\AppData\Roaming\Typora\typora-user-images\image-20210411094418914.png)



## 自动增量

![image-20210411093538561](https://raw.githubusercontent.com/KingdeGuo/myPictureBed/main/img_upload202104/11/093539-79270.png)

![image-20210411093609462](https://raw.githubusercontent.com/KingdeGuo/myPictureBed/main/img_upload202104/11/093612-911050.png)

- 上述图片中的`auto_increament`就是自动增量。
- 在每行添加到表中时，MySQL可以自动的为每行分配下一个可用编号，不用在添加时手动的分配唯一值。