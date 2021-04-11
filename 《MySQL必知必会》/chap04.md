[toc]

# 检索数据

- SQL语句不区分大小写

- 一般不适用`*`进行检索，检索不需要的列通常会降低加你所和应用程序的性能

- 使用`distinct`关键字去重，`select distinct columnname from tablename;`

  ![image-20210411185724247](https://raw.githubusercontent.com/KingdeGuo/myPictureBed/main/img_upload202104/11/185725-726956.png)

- 可以使用`limit`来限制结果

  - `limit 5`表示限制结果不超过5行，`select columnnname from table limit 5;`

  ![image-20210411190231165](https://raw.githubusercontent.com/KingdeGuo/myPictureBed/main/img_upload202104/11/190232-509203.png)

  - `limit 5 5`表示检索的开始行和行数，注意第一行用0表示，因此这相当于从第六行开始的5行。

  ![image-20210411190250701](https://raw.githubusercontent.com/KingdeGuo/myPictureBed/main/img_upload202104/11/190251-505328.png)

  - `limit 4 offset 3`等价于`limit 3, 4`

  ![image-20210411190337758](https://raw.githubusercontent.com/KingdeGuo/myPictureBed/main/img_upload202104/11/190339-397655.png)

