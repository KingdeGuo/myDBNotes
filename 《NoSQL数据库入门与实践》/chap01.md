[toc]

# NoSQL基础部分

- NoSQL的概念：主体符合非关系型、分布式、开放源代码和具有横向扩展能力的下一代数据库。

- NoSQL英文名称是`Not only SQL`，意思是：不仅仅是SQL。

- 数据库的分类

  ![image-20210425195359236](https://raw.githubusercontent.com/KingdeGuo/myPictureBed/main/img_upload202104/25/195400-120581.png)

  - TRDB是指：Traditional Relational Database，即 传统型关系型数据库

- 传统关系型数据库特点

  - 使用强存储模式技术
  - 采用SQL技术标准来定义和操作数据库
  - 采用强事务保证可用性和安全性
  - 主要采用单机集中式处理

  常采用下面的场景

  ![image-20210425201024587](https://raw.githubusercontent.com/KingdeGuo/myPictureBed/main/img_upload202104/25/201343-891333.png)

- NoSQL常见的五种模式

  ![image-20210425202437617](https://raw.githubusercontent.com/KingdeGuo/myPictureBed/main/img_upload202104/25/202441-981049.png)	- NoSQL的特点

  - 使用弱存储模式技术（少了一些约束，所以性能提升了）
  - 没有采用SQL技术标准来定义和操作数据库（所以可移植性不是很好）
  - 采用弱事务保证数据可用性即安全性或根本没有事务处理机制
  - 主要采用多机分布式处理
