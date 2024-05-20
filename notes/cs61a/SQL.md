建表：

```sql
create table [name] as [select statement];
select [expression] as [name]
```

```sql
create table parents as
  select 'a' as parent, 'b' as child union
  select 'a'		  , 'c'          union
  select 'f'          , 'a';
```

a是b，c的父母，f是a的父母

union表示上下列联合成一个表



查找：

```sql
select [columns] from [table] where [condition]
order by
```

```sql
select child from parents where parent = 'a';
select parent from parents where parent > child;
```



查找所有：

```
select * from parents
```

```
create table dogs as
	select 'b' as name, 'long' as fur;
create table parents as 
	select 'a' as parent,'b'   as child;

查询child列和name列相等时的结果：
>select * from parent, dogs where child=name;
>a|b|long

```



在上述查询中，没有一列的名称是模棱两可的。例如，很明显，name 列来自教练表，因为 big_game 表中没有名称为该列的列。但是，如果一个列名存在于不止一个被连接的表中，或者如果我们连接一个表与表本身，我们就必须使用别名来消除列名的歧义:

例如，让我们找出 big_game 中的一场比赛与之前任何一场比赛之间每支球队的比分差距。由于该表中的每一行代表一场比赛，因此要比较两场比赛，我们必须将 big_game 与它自己连接起来：

```
sqlite> SELECT b.Berkeley - a.Berkeley, b.Stanford - a.Stanford, a.Year, b.Year
...>        FROM big_game AS a, big_game AS b WHERE a.Year < b.Year;

```



