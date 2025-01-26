# Azure-File-Sync

### Let's Learn how to use Azure-File-Sync

# Summary

**Azure File Sync** lets you store your files in Azure and keep them in sync with your on-premises Windows servers. It helps:  

- Keep frequently used files on local servers for fast access.  
- Move less-used files to the cloud to save space.  
- Sync files across multiple locations automatically.  

It’s great for saving storage costs while still having local access to important files.

# Scenario:
This project demonstrates setting up Azure File Sync with an Azure VM acting as a client. A local partition and folder are created on the VM with full access permissions. Azure File Sync is then configured to synchronize the folder’s data with Azure, ensuring seamless and efficient data transfer between the local folder and Azure File Storage.

## Step - 1

*Create a VM*

i. Make sure you note which Windows Server you are using, as it will be required later in the process.

![image alt](https://github.com/Imaad-Mukadam/Azure-File-Sync/blob/5091d65eb51036a00aea94862336b9b5a07fb038/1.PNG)

ii. *fill up the basic coonfiguration and do Review and create*

iii. *Download the RDP file and connect to your created VM*

![image alt](https://github.com/Imaad-Mukadam/Azure-File-Sync/blob/9264f8fc21bc809904b81b7c5e04fe2b9a2cad5f/2.PNG)

iv. *Once the connection is done create a small partion*

![image alt](https://github.com/Imaad-Mukadam/Azure-File-Sync/blob/7f439f09f50344bbf10bf757cba7b0a3adf44c3d/3.PNG)

v. *open the file manager and create a folder inside your created partiton*

![image alt](https://github.com/Imaad-Mukadam/Azure-File-Sync/blob/7f439f09f50344bbf10bf757cba7b0a3adf44c3d/4.PNG)

vi. *Now we will provide full permission to the folder, open the properties of the folder, click on sharing , click on advanced sharing*

![image alt](https://github.com/Imaad-Mukadam/Azure-File-Sync/blob/7f439f09f50344bbf10bf757cba7b0a3adf44c3d/5.PNG)

vii. *Now click on share this file and then click on permission*

![image alt](https://github.com/Imaad-Mukadam/Azure-File-Sync/blob/7f439f09f50344bbf10bf757cba7b0a3adf44c3d/6.PNG)

viii. *Tick both the check boxes, then apply and OK*

![image alt](https://github.com/Imaad-Mukadam/Azure-File-Sync/blob/7f439f09f50344bbf10bf757cba7b0a3adf44c3d/7.PNG)

## Step - 2

i. *Create a storage Account*

![image alt](https://github.com/Imaad-Mukadam/Azure-File-Sync/blob/a14ded4e88f4c196046705de3c9786a40452d40e/8.PNG)

ii. *Create file share*

![image alt](https://github.com/Imaad-Mukadam/Azure-File-Sync/blob/796e028eb732c899273f510ed1ad23f3fc829600/9.PNG)

iii. *Configure the basic details of share file, and click on create*

![image alt](https://github.com/Imaad-Mukadam/Azure-File-Sync/blob/796e028eb732c899273f510ed1ad23f3fc829600/10.PNG)

## Step - 3

i. *Now, Search for fileSync*

![image alt](https://github.com/Imaad-Mukadam/Azure-File-Sync/blob/796e028eb732c899273f510ed1ad23f3fc829600/11.PNG)

ii. *Configure the basic, and hit create*

![image alt](https://github.com/Imaad-Mukadam/Azure-File-Sync/blob/796e028eb732c899273f510ed1ad23f3fc829600/12.PNG)

iii. *Once it is created , go to recourse, then go into sync group to create sync group*

![image alt](https://github.com/Imaad-Mukadam/Azure-File-Sync/blob/796e028eb732c899273f510ed1ad23f3fc829600/13.PNG)

iv. *Select your storage account and azure file share that you created*

![image alt](https://github.com/Imaad-Mukadam/Azure-File-Sync/blob/796e028eb732c899273f510ed1ad23f3fc829600/14.PNG)

v. *Once you created Sync group go to Registered Server to download a file Sync Agent That will help to create a communication between on-prem and azure*

![image alt](https://github.com/Imaad-Mukadam/Azure-File-Sync/blob/796e028eb732c899273f510ed1ad23f3fc829600/15.PNG)

vi. *Download the agent version based on the windows version you have selected during the creation of virtual machine*

![image alt](https://github.com/Imaad-Mukadam/Azure-File-Sync/blob/796e028eb732c899273f510ed1ad23f3fc829600/16.PNG)

vii. *Once the agent is downloaded copy it and paste into your virtual machine and install it (just click next,next)*

## Step - 4

i. *Go into Server Manager , local server and turnn off the Enchanced Security Configuration*

![image alt](https://github.com/Imaad-Mukadam/Azure-File-Sync/blob/796e028eb732c899273f510ed1ad23f3fc829600/18.PNG)

![image alt](https://github.com/Imaad-Mukadam/Azure-File-Sync/blob/796e028eb732c899273f510ed1ad23f3fc829600/17.PNG)

ii. *Once the Installation of the agent is done click on the sign in button*

![image alt](https://github.com/Imaad-Mukadam/Azure-File-Sync/blob/796e028eb732c899273f510ed1ad23f3fc829600/19.PNG)

ii. *CLick on the add button*

![image alt](https://github.com/Imaad-Mukadam/Azure-File-Sync/blob/796e028eb732c899273f510ed1ad23f3fc829600/20.PNG)

iii. *again click on the add button and close*

![image alt](https://github.com/Imaad-Mukadam/Azure-File-Sync/blob/796e028eb732c899273f510ed1ad23f3fc829600/21.PNG)

iv. *Provide your Azure gmail and Passowrd*

v. *Then select your subscription , resource group and Storage sync service then click on register buton*

![image alt](https://github.com/Imaad-Mukadam/Azure-File-Sync/blob/796e028eb732c899273f510ed1ad23f3fc829600/22.PNG)

## Step - 5

i. *Once Everything is done , check the Registered servers there will be your VM name , that means your VM is connected sucessfully*

![image alt](https://github.com/Imaad-Mukadam/Azure-File-Sync/blob/796e028eb732c899273f510ed1ad23f3fc829600/23.PNG)

ii. *Now open the Sync group , then click on your created Sync group , Click on Add server Endpoint*

iii. *Provide your VM name , Path of the folder that you want to be sync with the azure*

![image alt](https://github.com/Imaad-Mukadam/Azure-File-Sync/blob/796e028eb732c899273f510ed1ad23f3fc829600/24.PNG)

iv. *Now you will see the folder is successfully connected with the azure portal*

![image alt](https://github.com/Imaad-Mukadam/Azure-File-Sync/blob/796e028eb732c899273f510ed1ad23f3fc829600/25.PNG)

v. *To confirm the successfull connection , create some files and folders inside the folder of which you have given the path*

![image alt](https://github.com/Imaad-Mukadam/Azure-File-Sync/blob/796e028eb732c899273f510ed1ad23f3fc829600/26.PNG)

vi. *Now go into your file share(azure portal) , click on Browse , you will the files and folder that are created on the VM are in azure portal this means the Sync is succesfully done*

![image alt](https://github.com/Imaad-Mukadam/Azure-File-Sync/blob/796e028eb732c899273f510ed1ad23f3fc829600/27.PNG)



