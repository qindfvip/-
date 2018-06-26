# 随手笔记：
1）当firefox无法打开 https://addons.mozilla.org 时（因为墙），在系统配置文件hosts(ubuntu:/etc/hosts)添加以下配置即可访问
117.18.232.191 addons.cdn.mozilla.net<br/>
117.18.232.191 mozorg.cdn.mozilla.net<br/>
117.18.232.191 developer.cdn.mozilla.net<br/>
117.18.232.191 support.cdn.mozilla.net<br/>
117.18.232.191 marketplace.cdn.mozilla.net<br/>
117.18.237.191 getpersonas.cdn.mozilla.net<br/>
117.18.237.191 code.cdn.mozilla.net<br/>
117.18.232.191 air.cdn.mozilla.net<br/>
117.18.232.191 videos.cdn.mozilla.net<br/>
117.18.232.191 glow.cdn.mozilla.net<br/>
117.18.232.191 download-installer.cdn.mozilla.net<br/>
117.18.232.191 download.cdn.mozilla.net<br/>
117.18.232.191 fhr.cdn.mozilla.net<br/>
117.18.232.191 activations.cdn.mozilla.net<br/>
117.18.232.191 cdn.mozilla.net<br/>
117.18.232.191 snippets.cdn.mozilla.net<br/>
117.18.232.191 telemetry-experiment.cdn.mozilla.net<br/>
117.18.237.29 ocsp.digicert.com
<br/>

修改完后让配置文件生效（因为我是在ubuntu下），其他系统自行google<br/>
sudo /etc/init.d/networking restart
<br/>
2）linux下使用polipo实现全局代理<br/>
第一步安装：<br/>
sudo apt-get install polipo<br/>
第二步编辑配置文件：<br/>
proxyAddress = "0.0.0.0"<br/>
proxyPort = 8123  #polipo默认端口<br/>
<br/>
socksParentProxy = "127.0.0.1:1080"<br/>
socksProxyType = socks5<br/>
<br/>
chunkHighMark = 50331648<br/>
objectHighMark = 16384<br/>
<br/>
serverMaxSlots = 64<br/>
serverSlots = 16<br/>
serverSlots1 = 32<br/>
<br/>
第三步重启polipo:<br/>
sudo /etc/init.d/polipo restart<br/>
<br/>
第四步添加临时环境变量，如果想让其一直有效需要改环境变量配置文件<br/>
export http_proxy=127.0.0.1:8123<br/>
export https_proxy=127.0.0.1:8123<br/>
<br/>
第五步验证：<br/>
curl www.google.com
