[toc]

# 数据过滤

- 这一部分主要讲了`and`, `or`, `in`, `not in`这几个操作符。

- 操作符是指用来联结或改变`where`子句中的子句的关键字，也称为逻辑操作符。

- SQL会优先处理`and`，然后才会处理`or`，可以使用括号明确表示顺序

- 可以使用`in`操作符来指定条件范围，例如`in (1,2,3)`则会与条件1、2和3都进行匹配

  ![image-20210411193127441](https://raw.githubusercontent.com/KingdeGuo/myPictureBed/main/img_upload202104/11/193128-356820.png)

![image-20210411193209719](https://raw.githubusercontent.com/KingdeGuo/myPictureBed/main/img_upload202104/11/193422-114877.png)

![image-20210411193428887](https://raw.githubusercontent.com/KingdeGuo/myPictureBed/main/img_upload202104/11/193429-719402.png)

![image-20210411193645839](https://raw.githubusercontent.com/KingdeGuo/myPictureBed/main/img_upload202104/11/193646-146307.png)

- `in`操作符的优点
  - 语法直观、清楚
  - 计算的次序更容易管理
  - 一般比`or`执行效率更高
  - 可以包含其他`select`子句，能够动态的建立`where`子句。