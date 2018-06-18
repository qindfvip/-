# 当firefox无法打开 https://addons.mozilla.org 时（因为墙），在系统配置文件hosts(ubuntu:/etc/hosts)添加以下配置即可访问
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
