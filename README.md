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


