	[toc]

# 组合查询

- 有两种情况需要组合查询

  - 在单个查询中从不同的表返回类似结构的数据
  - 对单个表执行多个查询，按单个查询返回数据

- `union`将结果组合成单个结果集

  ![image-20210412154029747](https://raw.githubusercontent.com/KingdeGuo/myPictureBed/main/img_upload202104/12/154031-883539.png)

- 从`union`查询结果集中自动去除了重复的行，这是默认行为。如果希望显示所有的，可以使用`union all`而不是`union`