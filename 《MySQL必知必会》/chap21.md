[toc]

# 创建表

- 使用`create table`

  ![image-20210412174646133](C:\Users\asus\AppData\Roaming\Typora\typora-user-images\image-20210412174646133.png)

- `NULL`值就是没有值或者缺值。

- `primary key(key1, key2, ...)`设置主键

- `default 1`设置默认值为1

- `auto_increment` 自增键

  可以使用`insert`进行键的插入，只要它是唯一的即可，该值会被用来替代自动生成的值，后续的增量将开始使用该手工插入的值。

- 可以使用`select last_insert_id()`函数来获取最后一个`auto_increment`的值。

- 更新表用到的是`alter table`

  - 添加属性`alter table tablename add other_name char(20) `
  - 删除属性`alter table tablename drop column name`
  - 添加外键`alter table tablename add constraint the_key tablename foreign key (order_num) references orders (order_num);`

- 删除表可以使用`drop table tablename`

- 重命名表`rename table tablename to newname`；

