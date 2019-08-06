### MySQL

##### MySQL服务启动与关闭

```
方式1:计算机-右击管理-服务（找到mysql服务，手动启动）
方式2：通过管理员运行命令行---需要实践
net start 服务名 --启动服务
net stop 服务名 --关闭服务
方式3：Mysql Notifier
```

##### 常见命令

进入mysql命令行

```shell
mysql -u[用户名] -p[密码] [指定数据库]

-u 与用户名直接可以有空格，可以没有空格
-p 与密码直接不能有空格，如果不直接输入密码，则命令行会提示输入密码
[指定数据库] 指定要进入的数据库，默认进入根数据库
```

退出mysql命令行

```shell
mysql>exit
```

查看当前mysql版本

```shell
方式1：进入cmd命令行
      mysql --verison或者mysql -V
方式2：进入mysql命令行
      select version();
```

查看所有数据库列表

```shell
mysql> show databases;
```

进入指定数据库

```shell
mysql> use [数据库名称];
```

查看指定数据库中所有的表列表

```shell
mysql> show tables;
```

##### MySQL语法规范

```mysql
1：不区分大小写，但建议关键字大写，表名，列表小写
2：每条命令最后以“;”分号结尾
3：每条命令根据需要可以缩进或换行显示
4：注释
   单行注释：#注释文字
   单行注释：-- 注释文字 ,要注意有空格
   多行注释：/*注释文字*/
```



