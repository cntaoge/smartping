# Smartping Version 0.5.0
<li>程序官方网站： http://smartping.org/</li>
<li>项目地址： https://github.com/smartping/smartping</li></li>
<li>自己对页面进行了中文化，方便安装及备用</li>
<li>演示版地址：http://vpsjk.gxnnhxy.com:8899/</li>
----------------------------------------------------------
<br>安装环境：</br>
<p>Centos 7.x 64位 mini安装,登录系统后直接复制粘贴下面的命令</br>
<code><p>timedatectl set-timezone Asia/Shanghai</br>yum update -y</code></br>yum install git -y</code></br>git clone -b master https://github.com/cntaoge/smartping.git</br>chown -R root:root * smartping</br>chmod -R 755 *</br>chmod -R a+x smartping</br>echo "echo "cd /root/smartping;./control start" >>/etc/rc.d/rc.local</br>chmod +x /etc/rc.d/rc.local</br>cd smartping</br>./control start</br>#以下为CentOS 7系统防火墙规则</br>firewall-cmd --zone=public --add-port=8899/tcp --permanent</br>firewall-cmd --reload</br></code>
回车后，在浏览器上打开http://ip:8899 即可访问</br>
默认密码：smartping</br>
如需要修改默认的端口和密码，请先在监控平台的配置页面保存过一轮配置后，再用VI命令修改生成的配置文件</br>
<code>vi /root/smartping/conf/config.json</code></br>
“Port”: 8899,</br>
“Password”: “smartping”,</br>
<code>./control stop #停止程序</code></br>
<code>./control start #运行程序</code></br>
