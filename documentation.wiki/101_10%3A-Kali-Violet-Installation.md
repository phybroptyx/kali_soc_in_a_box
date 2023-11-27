# Prerequisites
[Kali Purple installation medium](https://www.kali.org/get-kali/)  
  
# Installation

Create Secure Server VLAN

![image](uploads/76efdb97b665b80c5182976ca2533645/image.png)  
![image](uploads/67458ee04a40ea4c3d920d13899c9597/image.png)  
![image](uploads/3c024ee5c2c6bd2455515b79cbdd3045/image.png)  
![image](uploads/11a7af32959364ae20d697a2aac14cf3/image.png)  
![image](uploads/e2bd9994537a862247f493baac5734c9/image.png)  
![image](uploads/1fc9ec5fe3028c03f9e60445e61fb110/image.png)  
![image](uploads/93d3204e9b1905f4c5082c5dde55d477/image.png)  
![image](uploads/32a2594924af9192a0973ff4dd96d78c/image.png)  
![image](uploads/5f839668d7da93e27e8691281b978456/image.png)  
![image](uploads/60e571c544368a4d8ed1b8921dd81c6e/image.png)  
![image](uploads/ce58504d6f1222c37ac55c3ce9c77391/image.png)  
![image](uploads/f67f78f36d1bbcf37551c91108a1aad0/image.png)  
![image](uploads/5b00d2307599d5abb141432dac50f2bc/image.png)  
![image](uploads/eebcffda56ddbcdba5a0963c7970a778/image.png)  
![image](uploads/f1971d9e9ffe96fa3851ed02a2cdc779/image.png)  
![image](uploads/3ac34d48018d86662a3309f29ddbcb94/image.png)  
![image](uploads/04ff8cd341478d87d54eb3427cc28d81/image.png)  
![image](uploads/c442afd29242b97afe2da7a77bc64f25/image.png)  
![image](uploads/17117f0612e5f31142d4e6ce8c333f2b/image.png)  
  
Enable ssh for remote administration:
--------------------------------------------

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
sudo systemctl enable ssh --now
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Install xrdp for remote administration:
---------------------------------------------

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
sudo apt update && sudo apt install xrdp
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
![image](uploads/533c5f5214a80040cd791d8e04b94df6/image.png)  



~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
sudo systemctl enable xrdp --now
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
![image](uploads/a80a9fd8ccf53ccf02419f55eb763af7/image.png)  




Fix xrdp error message on login:
![image](uploads/a15ae719cbfda3ca903745bcc6167  630/image.png)  


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
sudo wget -P /etc/polkit-1/localauthority/50-local.d https://gitlab.com/kalilinux/documentation/kali-purple/-/raw/main/101_kali-violet/overlays/etc/polkit-1/localauthority/50-local.d/45-allow-colord.pkla
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
![image](uploads/40b3ce95efe4f0ceeaf9b835b3bfae21/image.png)  



Enable serial console:
-------------------------


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
sudo vi /etc/default/grub ##Add:
## Kali Purple: Enable serial console
GRUB_CMDLINE_LINUX_DEFAULT="quiet console=ttyS0,115200n8 console=tty1"
GRUB_TERMINAL="serial console"
GRUB_SERIAL_COMMAND="serial --speed=115200 --unit=0 --word=8 --parity=no --stop=1"
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
![image](uploads/9cde896be220dddf08b1ef84d07dc5df/image.png)  




~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
sudo update-grub
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~




reboot

Finished