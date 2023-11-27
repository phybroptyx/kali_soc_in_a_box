# Dependencies
## Note: The Kali Purple Elastic Server must be operational at this stage
  
# Installation  
### Install dependencies

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
sudo apt install -y rsyslog
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


# Create agent policy
In Elastic, go to Management -> Fleet -> Agent policies
Select “Linux Server Policy” and click “Add Agent”
![image](uploads/23b95d2f59fe919fc79bb49f502e8333/image.png)  

Copy the content from the “Linux Tar” tab in section 3. Install Elastic Agent on your host" and
paste into the command line of Kali-Eminence and add “--insecure” to the end before executing:
![image](uploads/462ba19284ae130e428c71e08f553a74/image.png)  


Answer “Y” when prompted.

Once installed, Eleastic will confirm successful enrollment and data ingestion:
![image](uploads/991bd8e321762c30e7f0f268e48d4359/image.png)   
 



Now you can open the "[Metrics System] Host overview" dashboard and select the new host to confirm data ingestion is working fine:
![image](uploads/075d90b4d87780355f52b47c74fdc0b9/image.png)  

 
  
 Finished
 
 