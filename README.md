# ray-install

## xray
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
config
```
nano /usr/local/etc/xray/config.json
```
systemd service
```
systemctl enable xray
systemctl start xray
systemctl stop xray
systemctl restart xray
systemctl disable xray
```

## v2ray
Install & Upgrade v2ray-core and geodata
```
bash <(curl -L https://raw.githubusercontent.com/unionkx/ray-install/main/v2ray-install.sh)
```
Install & Upgrade geoip.dat & geosite.dat
```
bash <(curl -L https://raw.githubusercontent.com/unionkx/ray-install/main/v2ray-install-dat.sh)
```
Remove v2ray
```
bash <(curl -L https://raw.githubusercontent.com/unionkx/ray-install/main/v2ray-install.sh) --remove
```
config
```
nano /usr/local/etc/v2ray/config.json
```
systemd service
```
systemctl enable v2ray
systemctl start v2ray
systemctl stop v2ray
systemctl restart v2ray
systemctl disable v2ray
```

## BBR
```
sudo nano /etc/sysctl.d/99-bbr.conf

net.core.default_qdisc=fq
net.ipv4.tcp_congestion_control=bbr

sudo sysctl --system
lsmod | grep bbr
reboot
```
