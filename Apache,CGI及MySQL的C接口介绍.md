## Apache安装
   
* sudo apt-get update
* sudo apt-get install tasksel
* sudo tasksel

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
