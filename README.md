# ray-install

## xray
```
installed: /usr/local/bin/xray
installed: /usr/local/etc/xray/*.json

installed: /usr/local/share/xray/geoip.dat
installed: /usr/local/share/xray/geosite.dat

installed: /var/log/xray/access.log
installed: /var/log/xray/error.log

installed: /etc/systemd/system/xray.service
installed: /etc/systemd/system/xray@.service
```
### xray install
Install & Upgrade xray-core and geodata
```
bash -c "$(curl -L https://github.com/unionkx/ray-install/raw/main/xray-install.sh)" @ install
```
Update geoip.dat and geosite.dat only
```
bash -c "$(curl -L https://github.com/unionkx/ray-install/raw/main/xray-install.sh)" @ install-geodata
```
Install & Upgrade Xray-core to a pre-release version
```
bash -c "$(curl -L https://github.com/unionkx/ray-install/raw/main/xray-install.sh)" @ install --beta
```
Remove xray, except json and logs
```
bash -c "$(curl -L https://github.com/unionkx/ray-install/raw/main/xray-install.sh)" @ remove
```
Remove Xray, include json and logs
```
bash -c "$(curl -L https://github.com/unionkx/ray-install/raw/main/xray-install.sh)" @ remove --purge
```
```
systemctl enable xray
systemctl start xray
systemctl stop xray
systemctl restart xray
systemctl disable xray
```

## v2ray
```
installed: /usr/local/bin/v2ray
installed: /usr/local/bin/v2ctl
installed: /usr/local/share/v2ray/geoip.dat
installed: /usr/local/share/v2ray/geosite.dat
installed: /usr/local/etc/v2ray/config.json
installed: /var/log/v2ray/
installed: /var/log/v2ray/access.log
installed: /var/log/v2ray/error.log
installed: /etc/systemd/system/v2ray.service
installed: /etc/systemd/system/v2ray@.service
```
### v2ray install
Install & Upgrade v2ray-core and geodata
```
bash <(curl -L https://raw.githubusercontent.com/unionkx/ray-install/main/v2ray-install.sh)
```
Install & Upgrade geoip.dat & geosite.dat
```
bash <(curl -L https://raw.githubusercontent.com/v2fly/fhs-install-v2ray/master/install-dat-release.sh)
```
Remove v2ray
```
bash <(curl -L https://raw.githubusercontent.com/unionkx/ray-install/main/v2ray-install.sh) --remove
```
```
systemctl enable v2ray
systemctl start v2ray
systemctl stop v2ray
systemctl restart v2ray
systemctl disable v2ray
```

## BBR
```
echo "net.core.default_qdisc=fq" >> /etc/sysctl.conf
echo "net.ipv4.tcp_congestion_control=bbr" >> /etc/sysctl.conf
sysctl -p
lsmod | grep bbr
reboot
```
tcp_bbr                20480  0
