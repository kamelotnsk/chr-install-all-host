# Внимание: опасный скрипт! (warning: dangerous script!)
```
CHR_VERSION=6.40rc8
DISK_PATH=
INSTALLPATH=/dev/${DISK_PATH}

apt-get update &&
apt-get install -y unzip wget pv &&
wget http://download2.mikrotik.com/routeros/${CHR_VERSION}/chr-${CHR_VERSION}.img.zip &&
unzip chr-${CHR_VERSION}.img.zip &&
echo u > /proc/sysrq-trigger &&
pv chr-${CHR_VERSION}.img | dd of=$INSTALLPATH &&
reboot
```
```
/user set admin password=********
/ip address add address=A.B.C.D/24 interface=ether1
/ip route add gateway=A.B.C.1
```
