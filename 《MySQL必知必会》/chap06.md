[toc]

# 过滤数据

- 使用`where`关键字

  ![image-20210411191956271](https://raw.githubusercontent.com/KingdeGuo/myPictureBed/main/img_upload202104/11/191956-952734.png)

- 数据也可以在应用层过滤，但是这样往往需要查询出额外的数据，并且需要额外的网络贷款来进行传输。

- 上述例子使用的相等性检测，实际上支持更多的操作

  | 操作符  | 说明               |
  | ------- | ------------------ |
  | =       | 等于               |
  | <>      | 不等于             |
  | !=      | 不等于             |
  | <       | 小于               |
  | <=      | 小于等于           |
  | >       | 大于               |
  | >=      | 大于等于           |
  | between | 在指定的两个值之间 |

- `NULL`值不是0、空字符或者仅包含空格的字符串。

- `is null`和`is not null`

  ![image-20210411192754920](https://raw.githubusercontent.com/KingdeGuo/myPictureBed/main/img_upload202104/11/192756-764263.png)