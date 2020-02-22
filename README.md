# -XIAOMI
适合小米R3G和斐讯N1
1. 将pkg.tar文件下载至路由器
2. 执行 "tar -xvf pkg.tar -C /"。
3. 执行 "/etc/rc.common /etc/init.d/oray_phddns enable"。
4. 执行 "/etc/config/phtunnel/runpht"，启动phtunnel。
5. app中扫描二维码绑定使用（二维码有超时时间，如果绑定失
败重新执行第 4 步）。
6.在后台一直执行
nohup /etc/config/phtunnel/runpht > /var/log/phtunnel.log 2>&1 &
或者
/etc/init.d/oray_phddns start

7.文件读写
chmod -R 777  /etc/config/phtunnel
chmod -R 777 /etc/rc.common
chmod -R 777 /etc/oray_phddns/uninstall.sh
