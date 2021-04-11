[toc]

# 使用MySQL正则表达式

- MySQL提供的是正则表达的一个子集。

- 使用关键字`regexp`

  ![image-20210411195106475](https://raw.githubusercontent.com/KingdeGuo/myPictureBed/main/img_upload202104/11/195207-488431.png)

- `.`匹配单一字符

  ![image-20210411195204527](https://raw.githubusercontent.com/KingdeGuo/myPictureBed/main/img_upload202104/11/195205-858695.png)

- MySQL中的正则表达式匹配不区分大小写，为了区分大小写可以使用`binary`
- `|`表示选择
- `[]`匹配多个字符之一
- 匹配特殊字符使用`\\`进行转义。

