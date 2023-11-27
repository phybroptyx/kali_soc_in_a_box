# Dependencies
## Note: The Kali Purple Elastic Server must be operational at this stage

# Installation  
### 1. Install pfsense integration on fleet server:
--------------------------------------------------------
In Kibana, go to  

   Fleet -> Agent policies -> Fleet Server Policy
   
   ![image](uploads/3c828c822981b5bd444a3fc7b2d420b9/image.png)  
   



Click “Add integration”
Search for pfsense and select
![image](uploads/942a0b855619ef186d59cd8f5df37856/image.png)  


Click “Add pfsense”
![image](uploads/b5d5adbd37bcc66122cb8dd6a124256a/image.png)  


Set “Syslog host” to “0.0.0.0”
![image](uploads/03948d5b7e93e5aa5aa5b3f6083f0d83/image.png)  

Click “Save and continue”
![image](uploads/56076886a8e7c25f3bf3f76a4162ed36/image.png)  


Click “Save and deploy changes”
This will install the integration listening on UDP port 9001.
![image](uploads/353468b26fc75c2c3483366e5cb3d40b/image.png)  





### 2. Configure OPNSense to send suslogs to kali-purple.kali.purple on UDP port 9001:
------------------------------------------------------------------------------------------------------------------

![image](uploads/310c87a96f90dca2362693ddbb251f92/image.png)  
![image](uploads/3a53dd00bbf591c97292328ba37009b8/image.png)  
  
Data is now being ingested:  
![image](uploads/6ed748436709505465140c021ad19c34/image.png)  
