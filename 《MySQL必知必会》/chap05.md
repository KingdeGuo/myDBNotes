[toc]

# 排序检索数据

- 关系数据库设计理论认为，如果不明确规定排序的顺序，则不应该假定检索出的数据是顺序有意义。
- `order by a1, a2, ...`将按照`a1`, `a2`, `...`的顺序依次排序。

![image-20210411190928850](https://raw.githubusercontent.com/KingdeGuo/myPictureBed/main/img_upload202104/11/190930-597678.png)

- 降序排序使用的是`order by a1 desc`，如果要多个进行降序排列，**需要在每个后面都写**，`order by a1 desc, a2 desc, ...`

![image-20210411191213094](https://raw.githubusercontent.com/KingdeGuo/myPictureBed/main/img_upload202104/11/191216-482759.png)

- 默认使用的是升序排序，也可以使用`asc`关键字进行明确表示。

- 区分大小写与排序顺序

  问题是：`a`和`A`相同吗？`a`在`B`之前还是之后。

  这些问题不是理论问题，其答案取决于数据库如何设置。

  在字典排序系统中，`A`被视为与`a`相同，这是MySQL和大多数数据管理系统的默认行为。但是数据库管理员可以在需要时改变这种行为。如果数据库中包含了大量的外语字符，可能必须要这么做。

- 利用`order by`和`limit`往往可以找出最大值或者最小值。

