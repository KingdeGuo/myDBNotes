[toc]

# 全文本搜索

- MySQL中的三个引擎

  - MyISAM
    - 支持全文本搜索
    - 不支持事务
  - InnoDB
    - 不支持全文本搜索
    - 支持事务
  - MEMORY
    - 功能等于MyISAM，但由于数据存储在内存中，速度极快，特别适合做临时表。

- 混用引擎类型有一个大缺陷，外键不能跨引擎，及时用一个引擎的表不能引用具有使用不同引擎的表的外键。

- 在使用全文本搜索时，MySQL不需要分别查看每个行，不需要分别分析和处理每个词，MySQL创建指定列中各词的一个索引，搜索可以针对这些词进行。

- 一般在创建表时使用全文本搜索，使用`fulltext`

  ![image-20210412155626684](https://raw.githubusercontent.com/KingdeGuo/myPictureBed/main/img_upload202104/12/155627-82283.png)

  ​			![image-20210412155716760](https://raw.githubusercontent.com/KingdeGuo/myPictureBed/main/img_upload202104/12/155716-17279.png)

- 在定义之后，MySQL自动维护该索引，在增加、更新或删除行时，索引也随之自动更新。

- 不要在导入数据时使用`fulltext`。应该先导入数据，然后再修改表，定义`fulltext`，否则更新索引将会花费不少时间。

- 进行全文本搜索

  - `match()`指定被搜索的行
  - `against()`指定要使用的搜索表达式。

  ![image-20210412160245348](https://raw.githubusercontent.com/KingdeGuo/myPictureBed/main/img_upload202104/12/160808-854286.png)

- 查询扩展，使用`with query expansion`

  ```sql
  selcect note_text from productnotes where match（note_text) against('anvils' with query expansion);
  ```

- 布尔文本搜索，使用`in boolean mode`

  ```sql
  selcect note_text from productnotes where match（note_text) against('anvils' in boolean mode);
  ```

- 全文本布尔操作符

  - `+` 包含，词必须存在
  - `-` 排除，词不能出现
  - `>`包含，而且增加等级值
  - `<` 包含，而且降低等级值
  - `()` 把词组成子表达式
  - `~`取消一个词的排序值
  - `*`词尾通配符
  - `""`定义一个短语

  