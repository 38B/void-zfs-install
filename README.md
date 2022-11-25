### How to Use

Boot latest [hrmpf void linux iso](https://github.com/leahneukirchen/hrmpf/releases/latest)

```bash
$ loadkeys us
$ wpa_passphrase $SSID $PASSWORD >> /etc/wpa_supplicant/wpa_supplicant-$INTERFACE.conf
$ wpa_supplicant -B -i $INTERFACE -c /etc/wpa_supplicant/wpa_supplicant-$INTERFACE.conf
$ sv restart dhcpcd
$ ntpd
$ git clone https://github.com/38b/void-zfs-install
$ cd void-zfs-install
$ ./01-configure.sh
$ ./02-install.sh
```
