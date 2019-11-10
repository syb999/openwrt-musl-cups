# openwrt-musl-cups

for LEDE / OPENWRT 18.06 / OPENWRT 19.07 

----------------------------------------
下载对应平台.ipk文件，并上传至路由器/tmp目录内安装
opkg install /tmp/*.ipk

修改/etc/cupsd.conf文件:
-WebInterface NO
+WebInterface Yes

重启服务：
/etc/init.d/cupsd restart

使用http://lan_ip:631/admin登陆cups管理页面：
用户名：root
密码：你配置的路由器的登陆密码





