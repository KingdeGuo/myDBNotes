[toc]

# 使用数据处理函数

- 大多数的SQL移植性还是比较强的，但是函数的可移植性不强。

- 如果决定使用函数，最好能写上注释，方便别人理解。

- 部分函数举例

  - `upper()`转化为大写

  - `length()`返回串的长度

  - `locate()`找出串的一个字串

  - `ltrim()`去掉串左边的空格

  - `rtrim()`去掉串右边的空格

  - `soundex()`返回串`soundex`的值

    ![image-20210411212555859](https://raw.githubusercontent.com/KingdeGuo/myPictureBed/main/img_upload202104/11/212558-482249.png)

  - `substring()`返回字串的字符

  - `left()`返回串左边的字符

- 日期和时间处理函数

  - `adddate()`增加一个日期
  - `addtime()`增加一个时间
  - `curdate()`当前日期
  - `curtime()`当前时间
  - `date()`返回日期时间的日期部分
  - `datediff()`计算两个日期之差
  - `date_add()`日期运算函数
  - `date_format()`返回一个格式化的日期或时间串
  - `day()`返回日期的天数部分
  - `dayofweek()`返回对应的星期几
  - `hour()`返回小时部分
  - `minute()`返回分钟部分
  - `month()`返回月份部分
  - `now()`返回日期和时间
  - `second()`返回秒部分
  - `time()`返回日期的时间部分
  - `year()`返回日期的年份部分

- MySQL中的日期格式是`yyyy-mm-dd`

  ![image-20210411213335007](https://raw.githubusercontent.com/KingdeGuo/myPictureBed/main/img_upload202104/11/213336-117230.png)

- 可以使用`between and`进行连接查询

  ![image-20210411213501544](https://raw.githubusercontent.com/KingdeGuo/myPictureBed/main/img_upload202104/11/213501-822575.png)

- 常见的数值处理函数
  - `abs()`
  - `cos()`
  - `exp()`
  - `mod()`
  - `pi()`
  - `rand()`
  - `sin()`
  - `sqrt()`
  - `tan()`