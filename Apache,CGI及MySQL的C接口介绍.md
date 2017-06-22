## Apache安装
### 进入linux根目录下依次执行以下三条命令：
* sudo apt-get update
* sudo apt-get install tasksel
* sudo tasksel
### 完成以上操作输入mysql -u root -p回车输入密码进入mysql；

## 下载安装atom步骤

1. 在浏览器中输入atom.io进入下载界面
2. 找到atom-amd64.deb复制链接地址
3. 回到Linux在根目录下执行：wget -c 链接地址
4. 执行sudo dpkg -i atom-amd64.deb

## Apache开启CGI

1. 在apache中开启cgi支持
* sudo ln -s /etc/apache2/mods-available/cgi.load /etc/apache2/mods-enabled/cgi.load
2. 重启 apache 服务器
*  service apache2 restart
3. 运行的cgi文件的存放路径
* /usr/lib/cgi-bin
4. 改完目录的权限, 方便对目录下的文件写
* sudo mkdir /usr/lib/cgi-bin/sx
* sudo chmod 777 /usr/lib/cgi-bin/sx

## 安装mysql的C语言库

* sudo apt-get update
* sudo apt-get install libmysqlclient-dev
