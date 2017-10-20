#### 1. 端口修改问题
>1. 由于安装时默认端口为80，会和其他进程的端口冲突，所以必须修改，否则无法启动
>2. 修改方法为：修改`D:\study\wamp\bin\apache\apache2.4.9\conf`这个安装目录下的`httpd.conf`文件
>3. 查找listen，修改`Listen 0.0.0.0:80，Listen [::0]:80`这两个地方的端口为安装时的端口`8088`
***
#### 2. 无法登陆phpMyAdmin的问题
>1. 其实这个问题，无论是appserv，还是wamp都是会存在的
>2. 辣鸡百度，浪费我的时间，搜出来一堆答案，全都是互相抄袭，复制粘贴的，根本没有一个能解决实际问题
>3. 修改`D:\study\wamp\apps\phpmyadmin4.1.14`这个目录下的`config.inc.php`文件,注释掉第二行，打开第一行，第四行填上自己的数据库密码
```
1. $cfg['Servers'][$i]['auth_type'] = 'cookie';
2. $cfg['Servers'][$i]['auth_type'] = 'config';
3. $cfg['Servers'][$i]['user'] = 'root';
4. $cfg['Servers'][$i]['password'] = '*****';
```
>4. 打开浏览器登录，只输入用户名root，不输入密码，密码需要登入之后才能设置
>5. 至此，所有问题完美解决

**道阻且长，且行且珍惜！**
