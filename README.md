# Smartping Version 0.5.0
<p>程序官方网站： http://smartping.org/ </p>
<p>项目地址： https://github.com/smartping/smartping</p>
<p>自己对页面进行了中文化，方便安装及备用</p>
<p>演示版地址：http://vpsjk.gxnnhxy.com:8899/</p>
<p>----------------------------------------------------------</p>
<p>安装环境：</p>
<p>Centos 7.x  64位 mini安装,登录系统后直接复制粘贴下面的命令</p>

<code><p>timedatectl set-timezone Asia/Shanghai</p>
<p>yum update -y</p>
<p>yum install git -y</p>
<p>git clone -b master https://github.com/cntaoge/smartping.git</p>
<p>chown -R root:root * smartping</p>
<p>chmod -R 755 *</p>
<p>chmod -R a+x smartping</p>
<p>echo "cd /root/smartping;./control start" >>/etc/rc.d/rc.local</p>
<p>chmod +x /etc/rc.d/rc.local</p>
<p>cd smartping</p>
<p>./control start</p>
<p>#以下为CentOS 7系统防火墙规则</p>
<p>firewall-cmd --zone=public --add-port=8899/tcp --permanent</p>
<p>firewall-cmd --reload </p></code>

<p>回车后，在浏览器上打开http://ip:8899  即可访问</p>
<p>默认密码：smartping</p>

<p>如需要修改默认的端口和密码，请先在监控平台的配置页面保存过一轮配置后，再用VI命令修改生成的配置文件</p>
<code><p>vi /root/smartping/conf/config.json</p></code>

<p>“Port”: 8899,</p>
<p>“Password”: “smartping”,</p>

<code><p>./control stop #停止程序</p>
<p>./control start #运行程序</p></code>
