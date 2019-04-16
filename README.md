# Smartping Version 0.5.0
<p>程序官方网站： http://smartping.org/ </p>
<p>项目地址： https://github.com/smartping/smartping</p>
<p>自己对页面进行了中文化，方便安装及备用</p>
<p>演示版地址：http://vpsjk.gxnnhxy.com:8899/</p>
<p>----------------------------------------------------------</p>
<p>安装环境：</p>
<p>Centos 7.x  64位 mini安装,登录系统后直接复制粘贴下面的命令</p>

<li><code>timedatectl set-timezone Asia/Shanghai</li>
<li>yum update -y</li>
<li>yum install git -y</li>
<li>git clone -b master https://github.com/cntaoge/smartping.git</p>
<li>chown -R root:root * smartping</li>
<li>chmod -R 755 *</li>
<li>chmod -R a+x smartping</p>
<li>echo "cd /root/smartping;./control start" >>/etc/rc.d/rc.local</li>
<li>chmod +x /etc/rc.d/rc.local</li>
<li>cd smartping</li>
<li>./control start</p>
<li>#以下为CentOS 7系统防火墙规则</li>
<li>firewall-cmd --zone=public --add-port=8899/tcp --permanent</li>
<li>firewall-cmd --reload</code> </li>

<li>回车后，在浏览器上打开http://ip:8899  即可访问</li>
<li>默认密码：smartping</li>

<li>如需要修改默认的端口和密码，请先在监控平台的配置页面保存过一轮配置后，再用VI命令修改生成的配置文件</li>
<li><code>vi /root/smartping/conf/config.json</code></li>

<li>“Port”: 8899,</li>
<li>“Password”: “smartping”,</li>

<li><code>./control stop #停止程序</li>
<li>./control start #运行程序</code></li>
