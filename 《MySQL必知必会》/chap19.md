[toc]

# 插入数据

- 使用`insert`语句，`insert into tablename(a1, a2, ...) values(v1, v2, ...)`
- 如果数据检索是最重要的，则可以在`insert`和`into`之间添加`low_priority`关键字指示MySQL降低`insert`语句的优先级。
- 可以使用`insert select`结构来插入检索出来的数据