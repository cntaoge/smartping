# Smartping Version 0.5.0
<li>程序官方网站： http://smartping.org/</li>
<li>项目地址： https://github.com/smartping/smartping</li></li>
<li>自己对页面进行了中文化，方便安装及备用</li>
<li>演示版地址：http://vpsjk.gxnnhxy.com:8899/</li>
----------------------------------------------------------
<br>安装环境：</br>
<p>Centos 7.x 64位 mini安装,登录系统后直接复制粘贴下面的命令</p>
<p></p>
<p><code>timedatectl set-timezone Asia/Shanghai</code><code></code></p>
<p><code>yum update -y</code></p>
<p><code>yum install git -y</code></p>
<p><code>git clone -b master https://github.com/cntaoge/smartping.git</code></p>
<p><code>chown -R root:root * smartping</code></p>
<p><code>chmod -R 755 *</code></p>
<p><code>chmod -R a+x smartping</code></p>
<p><code>echo "echo "cd /root/smartping;./control start" >>/etc/rc.d/rc.local</code></p>
<p><code>chmod +x /etc/rc.d/rc.local</code></p>
<p><code>cd smartping</code></p>
<p><code>./control start</code></p>
#以下为CentOS 7系统防火墙规则
<code>firewall-cmd --zone=public --add-port=8899/tcp --permanent</code>
<code>firewall-cmd --reload</code>
<p></p>
回车后，在浏览器上打开http://ip:8899 即可访问
默认密码：smartping
如需要修改默认的端口和密码，请先在监控平台的配置页面保存过一轮配置后，再用VI命令修改生成的配置文件
<p></p>
<code>vi /root/smartping/conf/config.json</code>
“Port”: 8899,
“Password”: “smartping”,
<code>./control stop #停止程序</code>
<code>./control start #运行程序</code>
