[toc]

# 文件

## 都有哪些文件

- 参数文件
- 日志文件
- socket文件
- pid文件：MySQL实例的进程ID文件
- MySQL表结构文件
- 存储引擎文件：因为MySQL表存储引擎的关系，每个存储引擎都会有自己的文件来保存各种数据。这些存储引擎真正存储了记录和索引等数据。



## 参数文件

- 默认情况下，MySQL实例会按照一定的顺序在指定的位置进行读取，用户只需要通过命令`mysql --help | grep my.cnf`来寻找即可。

- MySQL实例可以不需要参数文件，这时所有的参数值取决于编译MySQL时指定的默认值和源代码中指定的参数的默认值。

- 如果MySQL实例在默认的数据库目录下找不到mysql架构，则同样启动失败。

- MySQL的mysql架构中记录了访问该实例的权限。

- 可以通过`show variables`查看数据库中的所有参数

  ![image-20210505095338293](https://raw.githubusercontent.com/KingdeGuo/myPictureBed/main/img_upload202105/05/095340-512434.png)
  - 在MySQL5.1之后还可以通过`information_schema`架构下的`GLOBAL_VARIABLES`视图来进行查找

  ```sql
  use information_schema;
  select * from global_variables where variable_name like 'innodb_buffer%'\G;
  ```

- MySQL中没有隐藏参数。

- MySQL数据库中参数可分为两类

  - 动态参数

    - 可以在实例中进行修改

    - 可以通过`SET`命令进行修改

      ```sql
      SET
      | [global | session] system_var_name = expr
      | [@@global. | @@session. | @@]system_var_name = expr
      ```

  - 静态参数：在整个实例的生命周期中不可以修改。

- 两个示例

  - 第一个

  ![image-20210505100508880](https://raw.githubusercontent.com/KingdeGuo/myPictureBed/main/img_upload202105/05/100510-759602.png)

  - 第二个

  ![image-20210505100625033](https://raw.githubusercontent.com/KingdeGuo/myPictureBed/main/img_upload202105/05/100626-244327.png)

- 需要注意的是，MySQL实例本身不会对参数文件中的该值进行修改，也就是在下次启动时还是会读取参数文件。若想在数据库实例下次启动时还是保留当前修改的值，那么用户必须去修改参数文件。



## 日志文件

