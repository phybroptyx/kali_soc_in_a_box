# Install dependencies
## Note: The Kali Purple Elastic Server must be operational at this stage  

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
sudo apt install -y rsyslog
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~




# Create fleet policy
In Elastic, go to Management -> Fleet -> Agent policies
Click create agent policy
Create policy called “Linux Server Policy”
![image](uploads/a97dab14b528c4b2e79a6b945da28705/image.png)  



Click “Create agent policy”
Back in the overview, click on the newly created policy and click “Add integration”
![image](uploads/1692a8d84dfa2147029b354577e6e6ae/image.png)  




Search for elastic agent and click add
![image](uploads/61c87ef93012c65123fe9c00308fb1cd/image.png)  
![image](uploads/f74de2fbe716876db77b21974e3d8ed0/image.png)  




When prompted, click on “Add elastic agent to your host”
![image](uploads/0138869cf542315d1ee2ee17e6b01942/image.png)  



Copy the content from the “Linux Tar” tab in section 3. Install Elastic Agent on your host"  
![image](uploads/77d5a7db565d29f1f84c87c2cc3e5585/image.png)  


paste into the command line of Kali-Violet and add “--insecure” to the end before executing:
![image](uploads/fd46a4dd29f275ce0d7255b54dd4b841/image.png)   


Answer “Y” when prompted.

Once installed, Eleastic will confirm successful enrollment and data ingestion:
![image](uploads/352668091e0dba6faec7bb171c16d96a/image.png)   
 



Now you can open the "[Metrics System] Host overview" dashboard and select the new host to confirm data ingestion is working fine:
![image](uploads/b4a73aaaff515cd4367e47a0efbb410d/image.png)  

 
 
 
 Finished
 
 