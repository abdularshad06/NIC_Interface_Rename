# NIC_Interface_Rename
Change NIC Interface Name


How to Change NIC Name in Linux CentOS 7

1)	ifconfig

 

2)	cd /etc/udev/rules.d/
3)	ls
 

4)	mv 90-eno-fix.rules 90-eno-fix.rules.bkp
5)	vim /etc/udev/rules.d/70-persistent-net.rules
SUBSYSTEM=="net", ACTION=="add", DRIVERS=="?*", ATTR{address}=="00:0c:29:52:ca:3b",ATTR{dev_id}=="0x0", ATTR{type}=="1", KERNEL=="ens*", NAME="eth0"

 

6)	cd /etc/sysconfig/network-scripts/
7)	mv ifcfg-eno16777736 ifcfg-eth0
8)	change to eth0 device and name in file
 

9)	Save and Exit
10)	reboot
