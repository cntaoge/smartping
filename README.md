# Smartping Version 0.5.0
<li>程序官方网站： http://smartping.org/</li>
<li>项目地址： https://github.com/smartping/smartping</li></li>
<li>自己对页面进行了中文化，方便安装及备用</li>
<li>演示版地址：http://vpsjk.gxnnhxy.com:8899/</li>
----------------------------------------------------------
<br>安装环境：</br>
<p>Centos 7.x 64位 mini安装,登录系统后直接复制粘贴下面的命令</br>
<p><code>timedatectl set-timezone Asia/Shanghai</br>
<p>yum update -y</code></br>
<p>yum install git -y</code></br>
<p>git clone -b master https://github.com/cntaoge/smartping.git</br>
<p>chown -R root:root * smartping</br>
<p>chmod -R 755 *</br>
<p>chmod -R a+x smartping</br>
<p>echo "echo "cd /root/smartping;./control start" >>/etc/rc.d/rc.local</br>
<p>chmod +x /etc/rc.d/rc.local</br>
<p>cd smartping</br>
<p>./control start</br>
<p>#以下为CentOS 7系统防火墙规则</br>
<p>firewall-cmd --zone=public --add-port=8899/tcp --permanent</br>
<p>firewall-cmd --reload</code></br>

回车后，在浏览器上打开http://ip:8899 即可访问</br>
默认密码：smartping</br>
如需要修改默认的端口和密码，请先在监控平台的配置页面保存过一轮配置后，再用VI命令修改生成的配置文件</br>
<code>vi /root/smartping/conf/config.json</code></br>
“Port”: 8899,</br>
“Password”: “smartping”,</br>
<code>./control stop #停止程序</code></br>
<code>./control start #运行程序</code></br>
