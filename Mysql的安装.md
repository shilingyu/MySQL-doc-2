# MySQL安装与配置
### MySQL介绍
MySQL是一个关系型数据库管理系统，是最流行的关系型数据库管理系统之一。在WEB应用方面，MySQL是最好的RDMS应用软件。
MySQL是一种关系数据库管理系统，关系数据库将数据保存在不同的表中，而不是将所有数据放在一个大仓库内，这样就增加了速度并提高了灵活性。 
MySQL所使用的 SQL 语言是用于访问数据库的最常用标准化语言。
MySQL是开源的，支持大型的数据库，允许于多个系统上，并且支持多种语言。
### MySQL安装配置
1. 更新源
   * 用vim打开源列表文件，使用命令：sudo vim /etc/apt/sources.list
   * 将以下源码粘贴到源列表里：   
   deb http://mirrors.aliyun.com/ubuntu/ xenial main restricted universe multiverse   
   deb http://mirrors.aliyun.com/ubuntu/ xenial-security main restricted universe multiverse   
   deb http://mirrors.aliyun.com/ubuntu/ xenial-updates main restricted universe multiverse   
   deb http://mirrors.aliyun.com/ubuntu/ xenial-backports main restricted universe multiverse   
   `##` 测试版源   
   deb http://mirrors.aliyun.com/ubuntu/ xenial-proposed main restricted universe multiverse
   `#`  源码   
   deb-src http://mirrors.aliyun.com/ubuntu/ xenial main restricted universe multiverse   
   deb-src http://mirrors.aliyun.com/ubuntu/ xenial-security main restricted universe multiverse   
   deb-src http://mirrors.aliyun.com/ubuntu/ xenial-updates main restricted universe multiverse   
   deb-src http://mirrors.aliyun.com/ubuntu/ xenial-backports main restricted universe multiverse 
   `##` 测试版源   
   deb-src http://mirrors.aliyun.com/ubuntu/ xenial-proposed main restricted universe multiverse   
   `#` Canonical 合作伙伴和附加   
   deb http://archive.canonical.com/ubuntu/ xenial partner   
   deb http://extras.ubuntu.com/ubuntu/ xenial main
2. Ubuntu安装MySQL  
   1. 执行sudo apt-get update更新源  
   2. 执行sudo apt-get install mysql-client mysql-server 安装mysql服务器和客户端   
   3. 执行sudo /etc/init.d/mysqld start 启动mysql服务 
3. Apache安装  
   1. 执行sudo apt-get update更新源  
   2. 执行sudo apt-get install tasksel 安装mysql服务器和客户端   
   3. 执行sudo tasksel   
   4. 进入以后空格键选中LAMP server，按下Tab键，回车，输入用户名root，密码123456   
   5. 检查数据库是否连接成功，执行mysql -u root -p，回车输入密码123456，回车，进入MySQL安装成功
4. 安装workbench  
   1. 执行命令sudo apt-get install mysql-workbench    
   2. 执行mysql-workbench进入mysql-workbench，安装成功
5. MySQL的使用
   * 打开终端命令
   * 在终端命令行执行命令：mysql –u root –p 回车输入密码123456
   * 进入mysql命令 ，对数据库的操作命令有：
   * 创建数据库，执行命令：create database <数据库名>;
   * 显示数据库，执行命令：show databases;
   * 删除数据库，执行命令：drop database <数据库名>;
   * 使用数据库，执行命令：use <数据库名>;
   * 创建数据库表，执行命令：create table <表名>(<字段名1><类型1>[,…<字段名n>]);
   * 表中插入数据，执行命令：insert into <表名> values(值1,…,值n);
   * 查询表中数据，执行命令：select [属性] from [表名] where 条件
   * 修改表中数据，执行命令：update set 字段=新值,…where 条件
   * 增加表中字段，执行命令：alter table 表名 add 字段 类型;
