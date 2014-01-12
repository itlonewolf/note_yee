安装插件
在离线模式下安装插件
help项目下


搭建服务器
#新建文件夹
	$mkdir svncode
#切换到刚创建的文件夹中
	$cd svncode
#在当前文件夹下创建仓库
	$svnadmin create .
#执行完成之后会出现四个文件夹，配置在conf文件夹中
	$cd conf
#文件中\#开头的都是注释行
#去掉
	auth-access = write
#之前的\#和空格
#以下两行都是如此，注意一定不要有空格
	password-db = passwd
	authz-db = authz
#修改完成之后保存退出
#修改passwd文件，配置用户名和密码，保存退出
#在authz文件最后写上
	[/]
	用户名 = rw
	* = r
#然后保持退出
#回到命令行
	$svnserve -d -r .
#-d表示后台 -r后面表示仓库的位置
#然后查看自己的ip地址
	$ifconfig
#192.168.104.209

#新建项目
#右键项目，选择team项的share Project，选择svn
#输入资源库位置
URL:svn://用户IP地址


#星号代表有改动，问号表示没有纳入到管理当中
#gen文件夹和bin都需要被忽略掉
#然后右键整个项目，然后选择commit，然后做一些注释
#作出改动之后，先更新再提交
	$killall server


	
	 
