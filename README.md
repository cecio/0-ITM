

![Screenshot](img/logo.png)

## Portable  Malware Analysis Tool

This is the repository for a Raspberry Pi 0 based distro, built to be a malware analysis lab. Main features are:

+ analysis of infected PC where it's not obvious how to extract the malware
+ analysis of malware requiring a lot of human interaction
+ analysis of malware with strong anti VM functionalities
+ analysis, through the Wifi, of Android, iOS and in general IoT behaviors
+ highly portable and configurable
+ ready to use in a quick way (menu driven)
+ veeeery cheap
+ several operating mode: AP, station, sniffing mode
+ secure (internal net are not routed, in routed mode)
It has been specifically built for Android base software: it contains a customized version of fakenet-ng to handle Android requests.

## Download Link

Will be released soon

## Image hashes

2018-07 image
```
MD5:     1364506be639a447560c0ca7fd53e27c
SHA-1:   f891216dbe79ee7c5ea102a602b0f191302f248f
SHA-256: 823d59b18b4f73c2ff740b8be3ac4f39994cf1a1d8b82d59fe88ec47f9cbc8ab
```

## General infos

```Default User: pi
Default Password: Zeroitm   (change it, please!)
Default SSID: 0itm
Default SSID password: 0itm0nly   (change it, please!)

IP wifi: 192.168.10.1
IP wired: 192.168.0.1

SSH Listening on port: 22222
```
If you use an ethernet adapter, you may need to modify udev rules to match the MAC address of you own adapter:
```
/etc/udev/rules.d/70-persistent-net.rules
SUBSYSTEM=="net", ACTION=="add", DRIVERS=="?*", ATTR{address}=="XX:XX:XX:YY:YY:YY", ATTR{dev_id}=="0x0", ATTR{type}=="1", KERNEL=="eth*", NAME="eth0"
```
