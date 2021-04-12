[toc]

# 分组数据

- 创建分组，使用`group by`

  ![image-20210411215007092](https://raw.githubusercontent.com/KingdeGuo/myPictureBed/main/img_upload202104/11/215007-160614.png)

- `group by`子句可以包含任意数目的列，这使得能对分组进行嵌套，为数据分组提供更细致的控制。

- 如果在`group by`子句中嵌套了分组，数据将在最后规定的分组上进行汇总。

- `group by`子句中列出的每个列都必须是检索列或者有效的表达式（但是不能是聚集函数），如果在`select`中使用表达式，则必须在`group by`子句中使用相同的表达式，不能使用别名。

- 除聚集计算语句外，`select`语句中的每个列都必须在`group by`子句中给出。

- 如果分组中有`null`值，那么`null`将作为一个分组返回。如果有多行`null`，将被视为一个分组。

- `with rollup`可以得到每个分组以及每个分组汇总级别的值

  ![image-20210412150418828](https://raw.githubusercontent.com/KingdeGuo/myPictureBed/main/img_upload202104/12/150420-378563.png)

- `where`用于过滤行，`having`用来过滤分组。

- `where`在数据分组前进行过滤，`having`在数据分组后进行过滤，`where`排除的行不包含在分组中。

  ![image-20210412150721174](https://raw.githubusercontent.com/KingdeGuo/myPictureBed/main/img_upload202104/12/150721-602082.png)

- 一般在使用`group by`时，会同时使用`having by`