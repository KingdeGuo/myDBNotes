[toc]

# 更新和删除数据

- 在更新或者删除的时候一定要使用`where`，否则可能造成所有数据的修改。

- `update table tablename set a1 = 'hello' where id=3`

  ![image-20210412172033921](C:\Users\asus\AppData\Roaming\Typora\typora-user-images\image-20210412172033921.png)

- 如果使用`update`语句进行多行更新，并且在更新这些行中的一行或多行时出现一个错误，则整个`update`操作被取消。为了即使发生错误也可以继续进行，可以使用`ignore`关键字进行。

  ```sql
  update ignore table tablename set a1 = 'hello' where id=3
  ```

- 删除使用的是`delete`，`delete from tablename where id=3`

- `delete`删除表中的所有行，但是不会删除表本身。如果想要删除所有行，可以使用`truncate table`，这条语句更快。

- 保证每个表都有主键，尽可能像`where`子句那样使用它。

- 在对表使用`update`或者`delete`是可以先用`select`进行验证一下，保证过滤是数字是正确的。

- 使用强制实施引用完整性的数据库，这样MySQL将不允许删除具有其他表相关联的数据的行。

  