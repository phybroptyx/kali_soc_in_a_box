# Prerequisites
[Kali Purple installation medium](https://www.kali.org/get-kali/)  
  
# Installation

Create Secure Server VLAN
![image](uploads/128b0256b71a2ba51f1f5194d04a0f71/image.png)  
![image](uploads/50be8d478f92238a427715361f89b786/image.png)  
![image](uploads/f1e2328bd306236db1c4a4063a24447a/image.png)  

Create VM  
![image](uploads/6ade1dd19292af3cccb0f0aa311e658a/image.png)  
![image](uploads/97ea7dbe9b6d1addf97daedf152d0e25/image.png)  
![image](uploads/9766c4c20a72df3f158f1786366f599b/image.png)  
![image](uploads/81df93443f6fe5f87ea7843ed7aaaf33/image.png)  
![image](uploads/6521e73160540ecee16d1adbd3f8da88/image.png)  
![image](uploads/617a8a3fb646924efa7d34c2b975c089/image.png)  
![image](uploads/fca28dbad6e7b28c4879673268aa7036/image.png)  
![image](uploads/b6658daa7ddb9d094c81abca3b5a58c4/image.png)  
![image](uploads/96b0743890970f7e997275991c621c38/image.png)  
  
Install Kali Purple  
![image](uploads/c30fd78ed4b14e38f0fccaa8a23421c5/image.png)  
![image](uploads/5a996a2876fcb48b29e12c22e6fec903/image.png)  
![image](uploads/08a952538c7fd6991c978b1636287e90/image.png)  
![image](uploads/ee1b23313a89105171e240794fe14b49/image.png)  
![image](uploads/86d50e4a860daf4dcc0612f64b7bb873/image.png)  
![image](uploads/858e2937d7215501f1f59ab5dac7552b/image.png)  
![image](uploads/6782fb063344c47438111099d59c3eab/image.png)  
  
Create a large swap partition:  
![image](uploads/d446133e891631ddf9eda0dfe7ba1a83/image.png)  
![image](uploads/2fbb2f39e39ec746cd7cf770c2e92074/image.png)  
![image](uploads/d57181b1f9561736b52822e1124624f8/image.png)  
  
Enable serial console:  


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
sudo vi /etc/default/grub ## Add:
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~



~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
## Kali Purple: Enable serial console
GRUB_CMDLINE_LINUX_DEFAULT="quiet console=ttyS0,115200n8 console=tty1"
GRUB_TERMINAL="serial console"
GRUB_SERIAL_COMMAND="serial --speed=115200 --unit=0 --word=8 --parity=no --stop=1"
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
![image](uploads/26d424c69f25f16fe1bf17fb8a063ade/image.png)  





~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
sudo update-grub
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
![image](uploads/506df494c8cf579885f8ca0782778545/image.png)  
![image](uploads/01227afb87c0c43f410c852f3a4d2b4a/image.png)  


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
sudo systemctl enable ssh --now
sudo apt update && sudo apt full-upgrade
sudo apt install xrdp
sudo systemctl enable xrdp --now
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~




Fix xrdp error message on login:
![image](uploads/31d749672e04a40688d84d1678498cd1/image.png)  

sudo wget -P /etc/polkit-1/localauthority/50-local.d https://gitlab.com/kalilinux/documentation/kali-purple/-/raw/main/301_kali-purple/overlays/etc/polkit-1/localauthority/50-local.d/45-allow-colord.pkla
![image](uploads/8d3e4dbc539bd70d48f4f911eb9480d1/image.png)  





Finished











