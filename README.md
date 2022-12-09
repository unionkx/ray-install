# ray-install

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
### v2ray安装脚本
Install & Upgrade v2ray-core and geodata
```
bash <(curl -L https://raw.githubusercontent.com/unionkx/ray-install/master/v2ray-install.sh)
```

## xray
```
installed: /etc/systemd/system/xray.service
installed: /etc/systemd/system/xray@.service

installed: /usr/local/bin/xray
installed: /usr/local/etc/xray/*.json

installed: /usr/local/share/xray/geoip.dat
installed: /usr/local/share/xray/geosite.dat

installed: /var/log/xray/access.log
installed: /var/log/xray/error.log
```

### xray安装脚本
Install & Upgrade Xray-core and geodata
```
bash <(curl -L https://raw.githubusercontent.com/unionkx/ray-install/master/xray-install.sh)
```
