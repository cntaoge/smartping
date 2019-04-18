# Smartping Version 0.5.0
<li>感谢开源项目Smartping
<li>程序官方网站： http://smartping.org/
<li>项目地址： https://github.com/smartping/smartping
<li>自己仅对页面进行了中文版，方便安装及备用。
<li>中文版演示版地址：http://106.12.110.166:8899/
<li>欢迎大家一起交流，主站上有多种联系方式：www.gxnnhxy.com
<br>------------------------------------------------------------------------
<li>安装环境：</br>
Centos 7.x 64位 mini安装,脚本里的命令是自动安装在/home目录下，登录SSH后可以直接复制粘贴下面的命令：
<br>
<br>timedatectl set-timezone Asia/Shanghai
<br>rpm -Uvh http://dl.fedoraproject.org/pub/epel/6/x86_64/epel-release-6-8.noarch.rpm
<br>yum install golang -y
<br>cd /home
<br>git clone -b master https://github.com/cntaoge/smartping.git 
<br>chmod -R a+x /home/smartping
<br>chmod -R 755 /home/smartping
<br>chmod 777 /home/smartping/control
<br>cd /home/smartping;./control start
<br>firewall-cmd --zone=public --add-port=8899/tcp --permanent 
<br>firewall-cmd --reload
<br>echo "cd /home/smartping;./control start" >>/etc/rc.d/rc.local
<br>chmod +x /etc/rc.d/rc.local
<br>cd /home/smartping;./control restart
<br>ok
<p>
<li>添加到系统开机启动。命令格式：</br>
<p>
echo "cd /root/smartping;./control start" >>/etc/rc.d/rc.local</br>chmod +x /etc/rc.d/rc.local
<p>
<li>以下为CentOS 7系统防火墙规则：如果是在宝塔面板下直接在面板安全项中添加端口。命令格式：</br>
<p>
firewall-cmd --zone=public --add-port=8899/tcp --permanent
<br>firewall-cmd --reload
<p>
<li>访问监控平台页面</br>
在浏览器上打开  http://ip:8899   即可访问；默认密码：smartping</br>如需要修改默认的端口和密码，请先在监控平台的配置页面保存过一次设置后，系统会在smartping/conf/的目录下生成当前的配置文件config.json，再用VI命令修改生成的配置文件，如果是在宝塔面板下直接在面板文件管理中修改config.json。命令格式：</br>
<p>
vi /root/smartping/conf/config.json
<p>
<li>找到以下字符串并修改为你自己的要求</br>
<p>
“Port”: 8899,</br>“Password”: “smartping”,</br>
<li>修改完config.json需要重启程序才能生效。命令格式：</br>
<p>
cd /root/smartping;./control restart
<p>
系统的防火墙检查没问题了，还得注意一些云系统的第二道防火墙的安全组设置，那边也是需要打开相应的端口。</br>
