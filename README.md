# DEPLOY-SIMPLE-STATIC-WEBSITE-ON-GOOGLE-CLOUD-PLATFROM(GCP)-BY-USING-STORAGE_BUCKET.

"TASK 2(Video Link):- https://drive.google.com/file/d/1kfbO1cISb63TnjV0ivw7qdAxoaC1XOzK/view?usp=drive_link"

Deploy a Simple Static Website on GCP by using Cloud Stoarge Bucket.

Step 1:- Launch a New VM Instance (“Compute Engine”- Google Cloud).
Log in to Google Cloud Console, navigate to Compute Engine, and create a new VM instance, and Security Traffic & Cloud Key is taken default.
This instance will serve as your server.

![Create VM Instance on Google Cloud-Image](https://github.com/user-attachments/assets/8ea239db-0327-4b45-814d-c7686252fcc8)


Step 2:- Connect via SSH & Gain Root Access & Update Package Lists.
Use the SSH option in the Google Cloud Console to access your instance securely. This provides a command-line interface.
Run “sudo su”- to switch to the root user. This gives you administrative privileges needed for installations and configurations.
Execute “apt-get update”- to ensure your package lists are up-to-date, which is crucial for installing the latest software.




Step 3:- Install Apache2 & Check Apache Status.
Use “apt-get install apache2” - to install the Apache server, which will host your web application or static website.
Verify Apache is running by using - “systemctl status apache2” or “service apache2 status”. This ensures your server is active and ready.




Step 4:-Create a Storage Bucket & Upload Files to the Bucket.
Navigate to the Cloud Storage page.
Click Create Bucket.
Set the Bucket name (must be globally unique).
Choose the Storage class and Location based on your needs.
Configure permissions (e.g., allow public or private access) & Click Create. 


Go to your bucket.
Click Upload Files or Upload Folder.
Select the file(s) from your local machine and upload.


Step 5:-Copy File from Cloud Storage to VM Instance
Use the gsutil command to copy the file from the bucket to the VM:
--“gsutil cp gs://sachin-bg01/one-page-website/*  /var/www/html”
-sachin-bg01 with the name of storage bucket.
-one-page-website with the name of the uploaded file.
-/var/www/html with the destination directory on our VM instance.

Step 5:- OUTPUT - Deploy Static Web Application.
Copy the public IP address of your VM, open a browser, and navigate to it. Your application should now be running.














