# Prerequisites
[Kali Purple installation medium](https://www.kali.org/get-kali/)  
  
# Installation

Create Secure Server VLAN
![image](uploads/7e410b3787e46e57af40754cb424b1fe/image.png)  
![image](uploads/9175b935eeb1522816d0047731c4837d/image.png)  
![image](uploads/325c3db36503bd75024d0a9644fa4aa6/image.png)  
![image](uploads/9a19071311beab0681cbad7435229ddc/image.png)  
![image](uploads/89950d57652ee984b43e251b896c4941/image.png)  
![image](uploads/1a8ff5f9a34fc75dfb4a5955b2b8a566/image.png)  
![image](uploads/e921dc99dd0923f061463c01ebce0ec0/image.png)  
![image](uploads/268c2cf2a082fab9c714e3c0e1a84716/image.png)  
![image](uploads/88bc873d32a261428f536fa61f3bfca6/image.png)  
![image](uploads/da2a407005f9491ac5099200a8c88cec/image.png)  
![image](uploads/e5822a35558d2f20ac4ed47ecbb637db/image.png)  
![image](uploads/236af5c6b74dc75b25d2d1df3fe27ded/image.png)  
  
Forgot to enter the name previously, so let's do that now:  
![image](uploads/a4090d054c644bdd0ca0ca18c21fbf5c/image.png)  

Enable serial console:  
![image](uploads/2c2ccf7e9849a618b61fa351e83fa2a1/image.png)  


Install Kali Purple:
![image](uploads/1ca9beeb36848d19a06bdf2837a88f46/image.png)
![image](uploads/8b50d87a3f8769e5695609baa8d37f64/image.png)  
![image](uploads/df6fa71c74ca372a6aeebb0c729d2166/image.png)  
![image](uploads/6e995ecb485ac0e5b8a7f04fc3577798/image.png)  
![image](uploads/533877fba7706d75fb391906b197710e/image.png)  
![image](uploads/9e5ea615a48f61b106a44d2a089f7ff8/image.png)  
![image](uploads/ce451e5e6e60b706cdc4051838614f7a/image.png)  
![image](uploads/6735861e7250d86d03bc99b653f1e08c/image.png)  
![image](uploads/c0ed24dc9cb62bea5c270c8d4455f5a4/image.png)  
  
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
![image](uploads/99ccaf9a385c89f3f2b66a17c9403e26/image.png)  



~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
sudo systemctl enable xrdp --now
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

![image](uploads/a84093a32d3aaec9f8dcc60813c11c99/image.png)  



Fix xrdp error message on login:
![image](uploads/a6db583a4b62ba6c762c0205520d6524/image.png)  


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
sudo wget -P /etc/polkit-1/localauthority/50-local.d https://gitlab.com/kalilinux/documentation/kali-purple/-/raw/main/401_kali-eminence/overlays/etc/polkit-1/localauthority/50-local.d/45-allow-colord.pkla
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

![image](uploads/d3b1cdea3469d20d679d44f0b57d7bf3/image.png)  


Enable serial console:
-------------------------


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
sudo vi /etc/default/grub ##Add:

## Kali Purple: Enable serial console
GRUB_CMDLINE_LINUX_DEFAULT="quiet console=ttyS0,115200n8 console=tty1"
GRUB_TERMINAL="serial console"
GRUB_SERIAL_COMMAND="serial --speed=115200 --unit=0 --word=8 --parity=no --stop=1"
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
![image](uploads/6f8efd9de1f6181dbc8e652c998554ea/image.png)  




~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
sudo update-grub
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

![image](uploads/39f979782a733076a78e0554a764ebc2/image.png)  
![image](uploads/58e69207d1f182ae1a6c622958b33c9d/image.png)  



Finished