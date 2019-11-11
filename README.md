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


-------------------------------------------

根据 https://oldwiki.archive.openwrt.org/doc/howto/cups.server?s[]=cups

1. kmod-usb-printers可能与cups存在兼容问题，请使用下面命令卸载kmod-usb-printers：
rmmod usblp.ko

2. 修改/etc/cups/cupsd.conf:
-User Nobody
-Group NObody
+User root
+Group root

3. chmod 700 /usr/lib/cups/backkend/usb

为了使用网络中其他客户端的打印机，必须共享打印机。在Web GUI中，添加打印机时应选中该复选框"Share This Printer"。






