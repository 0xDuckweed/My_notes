# SQL(Structrued Query Language)

### 1.数据库基础
+ 表（table）：特定类型数据的结构化清单
+ 模式（schema）：关于数据库和表的布局及特性的信息
+ 列（column）：表的字段，一个或多个列
+ 数据类型（datatype）：允许什么类型的数据，每个表列都有相应的数据类型，它限制（或允许）该列中存储的数据
+ 行（row） ：表中的一个记录
+ 主键（primary key） ：一列（或几列），其值能够唯一标识表中每一行
+ 关键字（keyword） ：作为 SQL 组成部分的保留字。关键字不能用作表或列的名字。
+ 不区分大小写
 
### 2.检索数据
+ SELECT column FROM table：从表中提取某一列所有行
  + SELECT column1, column2,column FROM table：选三列
  + SELECT * FROM table：所有列
+ SELECT DISTINCT id FROM table：输出不重复的值
  + 包括DISTINCT后面所有字段
+ SELECT id FROM table LIMIT 5：输出前五行数据
  + MySQL、MariaDB、PostgreSQL 或者 SQLite，需要使用 LIMIT子句
  + SELECT id FROM table LIMIT 5 OFFSET 5 ：输出第五行，下面五行数据。limit行数 offset起点行
  + 第 0 行 ：第一个被检索的行是第 0 行，而不是第 1 行。因此，LIMIT 1 OFFSET 1 会检索第 2 行，而不是第 1 行
+ 注释
  + -- 两个连字符后跟单行注释 or # 后跟注释
  + /* 注释 */ ：多行注释

### 3.排序检索数据
+ ORDER BY 语句：后跟列名且数量一致，并且此子句要在最后出现
  + 也可以用列的序号代替列名，也可混合
  + 顺序排列：默认为升序，降序需指定DESC关键字
    + 仅作用于DESC前的一个字段，多列需挨个指定

### 4.过滤数据
+ WHERE 子句：跟在table后面
  + 常用操作符
  + BETWEEN start AND end：闭区间
  + 空值NULL

### 5.高级数据过滤 
+ WHERE 组合 AND OR IN NOT 

### 6.通配符过滤
+ 针对未知值过滤，仅用于文本字段（字符串）
+ LINK 加通配符
+ 通配符
  +  % 匹配多个字符
  + _ 匹配单个字符
  + 集合通配符（部分不支持）

# MYSQL（RDBMS）
