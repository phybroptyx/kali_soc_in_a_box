# Prerequisites
[Kali Purple installation medium](https://www.kali.org/get-kali/), or  
[Kali Linux installation medium](https://www.kali.org/get-kali/)  
  
# Installation 
## 1. Create VM
![image](uploads/de2c51aa6b1d4136a2ae2d9e3e353dfe/image.png)  
![image](uploads/e160bc8d3eb177e61f3ddfdfef1b9822/image.png)  
![image](uploads/e109e110410b9c4585a49006b5b156ab/image.png)  
![image](uploads/93a7db6b2e873413e5cb227becfaf44c/image.png)  
![image](uploads/d5bce64f5424c00e61f2a849248144d5/image.png)  
![image](uploads/2ae0b41790f223f7a726dbe4cfbdc0cf/image.png)  
![image](uploads/5330deeeabfbaea9d67259f65c2766bc/image.png)  
![image](uploads/9ffae6c76144175273fe3e97926f319a/image.png)  
![image](uploads/c14de3ee23d9b413179ea053a7651903/image.png)  
![image](uploads/c4a5e56cad1e88538b906359bbf5401b/image.png)  
  
Standard Kali Linux or Kali Purple installation

Enable ssh for remote administration:
--------------------------------------------

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
sudo systemctl enable ssh --now
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
![image](uploads/68f63c326080b53078e0642a78ba74bb/image.png)  




Install xrdp for remote administration:
---------------------------------------------

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
sudo apt update && sudo apt install xrdp
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
![image](uploads/a1465b6a0ded84a00b4d091374236adb/image.png)  



~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
sudo systemctl enable xrdp --now
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
![image](uploads/2d47eb5de1185d729939e4e8f993bb53/image.png)  




Fix xrdp error message on login:
![image](uploads/c973e7bdb01e2a8acacc8f1b602c70ed/image.png)  


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
sudo wget -P /etc/polkit-1/localauthority/50-local.d https://gitlab.com/kalilinux/documentation/kali-purple/-/raw/main/1001_kali-heliotrope/overlays/etc/polkit-1/localauthority/50-local.d/45-allow-colord.pkla
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
![image](uploads/4e9c3ab08ae7d1de3240db0d66877f6f/image.png)  




Finished