[toc]

# 创建计算字段

- 使用`concat()`函数拼接字段

  - 中间使用`,`分开
  - `rtrim()`可以去掉右边所有的空格，`ltrimi()`去掉左边空格，`trim()`去掉两边空格

- 使用`as`起别名

  ![image-20210411201922238](https://raw.githubusercontent.com/KingdeGuo/myPictureBed/main/img_upload202104/11/201923-813766.png)

- 执行算术计算，例如`select price*2 from visitors;`

  