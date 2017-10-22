**本文参考自`http://www.cnblogs.com/jinjiyese153/p/6796668.html`**

**git软件下载自`http://blog.csdn.net/u011164906/article/details/59129835`**

>1. 下载安装git软件，安装过程中修改路径，并且把所有组件都安装上，其余选择第一项，或者默认
>2. 下载安装后打开gitbush，输入以下命令，设置用户名和邮箱
```
$ git config --global user.name "Your Name"
$ git config --global user.email "email@example.com"
```
>3. 在IDEA中设置Git，在File-->Setting->Version Control-->Git-->Path to Git executable选择你的git安装后的git.exe文件，然后点击Test，测试是否设置成功
>4. 在IDEA中设置GitHub，File-->Setting->Version Control-->GibHub
>     - Host：github.com
>     - Login:kwy112325
>     - Password:******
>5. 创建本地仓库，VCS-->Import into Version Control-->Create Git Repository...
>6. 在弹框中选中项目所在的位置，点击OK，此时项目文件全部变成红色
>7. 上传项目到本地仓库，项目右键选择Git-->add，此时项目文件变成绿色，此时文件只是处于暂存区，并没有真正进入到版本库中
>8. 项目右键Git--> Commit Directory，在弹窗中输入Commit Message，点击commit，此时项目文件从暂存区真正进入版本库中，项目文件变成白色
>9. 上传项目到GitHub中，VCS-->Import into Version Control-->Share Project on GitHub，在弹框中输入仓库名和描述，点击Share，即可是上传，中间会弹窗输入GitHub的用户名和密码（已输入过用户名和密码并记住的不会再次弹框输入），上传成功后IDEA右下角会给出提示
>10. 增添，修改，删除
>     - 新增文件（红色），右键-->Git-->add，将新增的文件加入本地仓库，此时文件变绿色
>     - 修改文件（蓝色）
>     - 在项目右键-->Git-->Commit Directory，查看有变动的文件并输入Commit Message，点击Commit and Push...
>     - 提交后会进行语法检查，若存在错误或警告会给出确认提示，点击Commit，弹出Push框，点击Push，上传GitHub成功

**道阻且长，且行且珍惜**
