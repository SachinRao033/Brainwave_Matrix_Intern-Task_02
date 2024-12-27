# DEPLOY-SIMPLE-STATIC-WEBSITE-ON-GOOGLE-CLOUD-PLATFROM(GCP)-BY-USING-STORAGE_BUCKET.

"TASK 2(Video Link):- https://drive.google.com/file/d/1kfbO1cISb63TnjV0ivw7qdAxoaC1XOzK/view?usp=drive_link"

## Deploy a Simple Static Website on GCP by using Cloud Stoarge Bucket.

### Step 1:- Launch a New VM Instance (“Compute Engine”- Google Cloud).

• Log in to the Google Cloud Console.   
• Navigate to Compute Engine → VM instances.   
• Click Create Instance.   
   --Set the instance name and specifications as needed.  
   --Keep Firewall rules as default for now.  
• Click Create to launch your instance.   
  
![Create VM Instance on Google Cloud-Image](https://github.com/user-attachments/assets/f5b00ef1-fa92-4ed9-8676-782b1eab06e4)
   

### Step 2:- Connect via SSH & Gain Root Access & Update Package Lists.   

• Use the SSH option in the Google Cloud Console to access your instance securely. This provides a command-line interface.  
• Run “sudo su”- to switch to the root user.   
• This gives you administrative privileges needed for installations and configurations.   
• Execute “apt-get update”- to ensure your package lists are up-to-date, which is crucial for installing the latest software.   
    
![Connect SHH-Image](https://github.com/user-attachments/assets/6f80ec8c-64e1-4932-a421-2b80779cf8d9)
  
![Root & Packages Update-Image](https://github.com/user-attachments/assets/9ac4cb9c-58fc-417b-99b0-70f22ebab940)
   

### Step 3:- Install Apache2 & Check Apache Status.   

• Use “apt-get install apache2” - to install the Apache server, which will host your web application or static website.   
• Verify Apache is running by using - “systemctl status apache2” or “service apache2 status”.    
• This ensures your server is active and ready.  
   
![Installing Apache2-Image](https://github.com/user-attachments/assets/323e70f7-c8df-449e-b2ee-64437cd69a1d)
    
![Apache2 Status-Image](https://github.com/user-attachments/assets/48d627f9-270d-44f2-b06c-9e6b1d597fbd)
  

### Step 4:-Create a Cloud Storage Bucket & Upload Files to the Bucket.   

• Go to the Cloud Storage section in the console.  
• Click Create Bucket.  
• Configure the bucket:  
    --Name: Provide a globally unique name.  
    --Storage Class: Select the appropriate class (e.g., Standard).  
    --Location: Choose the desired location.  
    --Set permissions (e.g., public or private access).  
• Click Create.  
  
![Bucket Created-Image](https://github.com/user-attachments/assets/4e476f4c-a7e9-4a3f-aa31-9eddadd07c31)

• Upload your static website files:  
 --Go to your bucket.   
 --Click Upload Files or Upload Folder.   
 --Select the file(s) from your local machine and upload.   
  
![Uploaded-Image](https://github.com/user-attachments/assets/1d4ddfa2-8a92-4762-ae90-8773fdd6139f)
   

### Step 5:-Copy File from Cloud Storage to VM Instance.   

• Use the gsutil command to copy the file from the bucket to the VM:
--“gsutil cp gs://sachin-bg01/one-page-website/*  /var/www/html”   
• -sachin-bg01 with the name of storage bucket.   
• -one-page-website with the name of the uploaded file.   
• -/var/www/html with the destination directory on our VM instance.   
  
![Copied to Bucket to VM Instance-Image](https://github.com/user-attachments/assets/e9b79a9d-e495-4c54-9e13-8a5e62ebba67)
   

### Step 5:- OUTPUT - Deploy Static Web Application.   
  
• Copy the external/public IP address of your VM instance.  
• Open a web browser and paste the IP address in the URL bar.  
• Your static website should now be live.  
   

![Copied Public IP-Image](https://github.com/user-attachments/assets/e6945777-8ba2-413b-9671-6621566d024c)
   

![Pasted on browser-image](https://github.com/user-attachments/assets/593a9ec9-f2f0-4890-95c7-1ddedab90fb9)
   

![Output Home-Image](https://github.com/user-attachments/assets/104d8cdc-879b-4d4c-b885-f7a0a1533517)
   

![Output-Image](https://github.com/user-attachments/assets/f86eaeb7-0935-4c44-85e4-98d76ae96d58)
   

![Output-Image](https://github.com/user-attachments/assets/85d26ba7-ae0a-4f78-ac47-8a8525a5a61a)
   

![Output-Image](https://github.com/user-attachments/assets/eceef70c-5465-4efb-bd98-f4abf5a7707f)
   

![Output-Image](https://github.com/user-attachments/assets/3230c715-cc81-425a-b513-917bbb467b12)

  
### Conclusion:

In this task, we successfully deployed a static website on Google Cloud using a virtual machine (VM) instance and Apache server. We began by creating a VM instance, then connected to it via SSH to gain root access and install Apache. After setting up the Apache server, we created a Cloud Storage bucket, uploaded our website files, and transferred them to the VM using the `gsutil` command. Finally, by accessing the VM's public IP, we verified that the static website was live and accessible from the web. This process provided hands-on experience with key cloud computing services such as Compute Engine and Cloud Storage, as well as deploying a basic static website in a cloud environment.    
  
