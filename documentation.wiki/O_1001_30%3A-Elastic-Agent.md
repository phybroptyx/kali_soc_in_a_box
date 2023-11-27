# Dependencies
## Note: The Kali Purple Elastic Server must be operational at this stage

# Installation  
### Install dependencies

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
sudo apt install -y rsyslog
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~



### Create agent policy
In Elastic, go to Management -> Fleet -> Agent policies
Click create agent policy
Create policy called “Linux Client Policy”
![image](uploads/6ccc136958eb91b4e037c9f892cdf017/image.png)  



Click “Create agent policy”
Back in the overview, click on the newly created policy and click “Add integration”

![image](uploads/013ee15a7f3cb4da04a65c50e002372f/image.png)  




Search for elastic agent and click add
![image](uploads/0d26ca59dbfe6bdf47079f0fac2a723a/image.png)  
![image](uploads/e9e44d53cb08e4472bee09d3021ca601/image.png)  




When prompted, click on “Add elastic agent to your host”

![image](uploads/d37c5ff6b26aabeeace9765a392f322b/image.png)  


Copy the content from the “Linux Tar” tab in section 3. Install Elastic Agent on your host"
![image](uploads/5e4d39680922829b207fb517f9dc802e/image.png)  


paste into the command line of Kali-Violet and add “--insecure” to the end before executing:
![image](uploads/695d5d43bb6eb71164dab234a66110d0/image.png)   


Answer “Y” when prompted.

Once installed, Eleastic will confirm successful enrollment and data ingestion:
![image](uploads/aa656e1c6a98d52593e87d897206b3f7/image.png)   
 


Now you can open the "[Metrics System] Host overview" dashboard and select the new host to confirm data ingestion is working fine:
![image](uploads/9dc63bdd2583e49f819a2a0bc08580b0/image.png)  

  
Finished
 
 