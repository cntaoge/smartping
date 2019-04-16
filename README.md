# Smartping Version 0.5.0
<li>程序官方网站： http://smartping.org/
<li>项目地址： https://github.com/smartping/smartping
<li>自己仅对页面进行了中文化，方便安装及备用
<li>演示版地址：http://vpsjk.gxnnhxy.com:8899/</br>
----------------------------------------------------------
<li>安装环境：</br>
Centos 7.x 64位 mini安装,登录系统后在root的文件目录下直接复制粘贴下面的命令：</br>
<p>
<code>timedatectl set-timezone Asia/Shanghai</br>yum update -y</br>yum install git -y</br>git clone -b master https://github.com/cntaoge/smartping.git</br>chmod -R 755 *</br>chmod -R a+x smartping</br>chmod -R 755 smartping</br>cd smartping</br>./control start</code></br>
<li>添加到系统开机启动</br>命令格式：</br>
<p><code>echo "cd /root/smartping;./control start" >>/etc/rc.d/rc.local</br>chmod +x /etc/rc.d/rc.local</code></br>
<li>以下为CentOS 7系统防火墙规则：如果是在宝塔面板下直接在面板安全项中添加端口</br>命令格式：</br>
<p><code>firewall-cmd --zone=public --add-port=8899/tcp --permanent</br>firewall-cmd --reload</code></br>
<li>访问监控平台页面</br>在浏览器上打开http://ip:8899 即可访问</br>默认密码：smartping</br>如需要修改默认的端口和密码，请先在监控平台的配置页面保存过一次设置后，系统会在smartping/conf/的目录下生成当前的配置文件config.json，再用VI命令修改生成的配置文件，如果是在宝塔面板下直接在面板文件管理中修改config.json。</br> 命令格式：</br>
<p><code>vi /root/smartping/conf/config.json</code></br>
<li>找到以下字符串并修改为你自己的要求</br>
<p>“Port”: 8899,</br>“Password”: “smartping”,</br>
<li>修改完config.json需要重启程序才能生效。</br>命令格式：</br>
<p>
<code>cd /root/smartping;./control restart</code></br>
