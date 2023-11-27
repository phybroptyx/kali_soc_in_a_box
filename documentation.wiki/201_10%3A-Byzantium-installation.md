# Prerequisites
Running PVE  
[OPNSense DVD image](https://opnsense.org/download/)  
  
# Installation  
![image](uploads/69a9bc21570456406f499f21bd90aa9c/image.png)  
![image](uploads/1179e55d0055f1aa82cf73ae40523db9/image.png)  
![image](uploads/e89b217a0deb4b82c6175fe3e43edb8f/image.png)  
![image](uploads/911c9991f3f47a44affee100a8fb669a/image.png)  
![image](uploads/d6daf424dba61806725dc442c6f3fb73/image.png)  
![image](uploads/ca161024a192ef665e24ac63f9f0f290/image.png)  
![image](uploads/a6bc60c2928ee6b825386c2e35e1a159/image.png)  
![image](uploads/5fad1e7046377a8886586cd6560e9196/image.png)  
![image](uploads/7562d61cf8194d2669952564130968dd/image.png)  
![image](uploads/966522b4d95a14a2e6b069913aae4824/image.png)  
![image](uploads/e5153780ad3c101cabc23d65ffcc7201/image.png)  
![image](uploads/ff89fef7dacc5732ccca8385fff53985/image.png)  
![image](uploads/9691f76a9b45fd2402ab08aeaa32761b/image.png)  
![image](uploads/1524bf3033632af396e531cbc5536d04/image.png)  
![image](uploads/98371fe70b6656e67a09d204dddd7f77/image.png)  
![image](uploads/9673626fd2c799600f2e52a1b75bdb4f/image.png)  
![image](uploads/b1a40c03fde6250c5cb1680f611d0aca/image.png)  
  
login: installer  
password: opnsense  
![image](uploads/99ef2632c225249e014faf531b978487/image.png)  
![image](uploads/eb342c312e8fb0b778752c1e50aafd18/image.png)  
![image](uploads/770e983c02cb8e73d56645d453dd2097/image.png)  
![image](uploads/40b9f95a03e3d6429cc7f8e6d5af18d6/image.png)  
![image](uploads/60d87ac401ec3b07d7bd6f6d2faca605/image.png)  
![image](uploads/59268291282ba3db9db17fa83900a818/image.png)  
![image](uploads/c65a1e010db97d700643d46bbf6a9bdd/image.png)  
![image](uploads/c0f8e47ec1ad32c1a981c4e22e0805e9/image.png)  
  
Configure LAN IP Address:  
![image](uploads/15a8f9fba9fe31b6864563aa143460a9/image.png)  
![image](uploads/fd03deef41a5de607ba5ec04ea069bbe/image.png)  
![image](uploads/324a95301e0f4e26ebcc57aca5544c70/image.png)  
![image](uploads/8806965dcd62062f0ec28681728b1a46/image.png)  
![image](uploads/a4e4bdf4cd3d17071530bc923e94dfe6/image.png)  
![image](uploads/a832efa0f4dbc2eb8e5e2bcfa654bfda/image.png)  
![image](uploads/695b813f99197770ccc59ac9fd712671/image.png)  
![image](uploads/45a08e4dba1b1e46068d5855b7eac18a/image.png)  
![image](uploads/47429665d0569a2c009df9641550c6f0/image.png)  
![image](uploads/56c35754043cda63feb608ea5b82b237/image.png)  
![image](uploads/47ad6413ff12624729c5554b57854110/image.png)  
![image](uploads/3116fe5bb0f2c55ce5891a11141349af/image.png)  
  
Use https://dns.watch/ dns servers for best privacy:  
DNS servers:  
84.200.69.80  
84.200.70.40  
![image](uploads/7fd044b32347bad9da16e1de057d8228/image.png)  
![image](uploads/3a3f2db1f5f618ab8d286f60b2e6359d/image.png)  
![image](uploads/12ebcc9666a9516e499fe964eeddf19c/image.png)  
![image](uploads/b27a68c91de4b8848d3735f7033405d7/image.png)  
![image](uploads/05dd7a1319a50b233c03fe8ae73f23c6/image.png)  
![image](uploads/bbb1d0ac665c536c765dc7c3e7b2227e/image.png)  
![image](uploads/8497c256f10cb5f91d517a50f3074cf6/image.png)  
  
Enable serial console:  
-------------------------  
  
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
vi /boot/loader.conf
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


# Add:


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
## Add serial console for proxmox
boot_multicons="YES"
boot_serial="YES"
comconsole_speed="115200"
console="comconsole,vidconsole"
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
  
![image](uploads/366a06d811c1521f7b80dd5545a279b8/image.png)  


Finished
