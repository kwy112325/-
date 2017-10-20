#### 1. 端口修改问题
>由于安装时默认端口为80，会和其他进程的端口冲突，所以必须修改，否则无法启动
>修改方法为：修改'D:\study\wamp\bin\apache\apache2.4.9\conf'这个安装目录下的'httpd.conf'文件
>查找listen，修改Listen 0.0.0.0:80，Listen [::0]:80这两个地方的端口为安装时的端口8088
***
#### 2. 无法登陆phpMyAdmin的问题
>其实这个问题，无论是appserv，还是wamp都是会存在的
>辣鸡百度，浪费我的时间，搜出来一堆答案，全都是互相抄袭，复制粘贴的，根本没有一个能解决实际问题
>修改'D:\study\wamp\apps\phpmyadmin4.1.14'这个目录下的'config.inc.php'文件
>$cfg['Servers'][$i]['auth_type'] = 'cookie';
>//$cfg['Servers'][$i]['auth_type'] = 'config';
>$cfg['Servers'][$i]['user'] = 'root';
>$cfg['Servers'][$i]['password'] = '*****';
>注释掉第二行，打开第一行，第四行填上自己的数据库密码，然后打开浏览器登录，只输入用户名root，不输入密码，密码需要登入之后才能设置。
>至此，所有问题完美解决

且行且珍惜！
