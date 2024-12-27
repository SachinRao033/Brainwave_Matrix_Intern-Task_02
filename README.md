# DEPLOY-SIMPLE-STATIC-WEBSITE-ON-GOOGLE-CLOUD-PLATFROM(GCP)-BY-USING-STORAGE_BUCKET.

"TASK 2(Video Link):- https://drive.google.com/file/d/1kfbO1cISb63TnjV0ivw7qdAxoaC1XOzK/view?usp=drive_link"

Deploy a Simple Static Website on GCP by using Cloud Stoarge Bucket.

Step 1:- Launch a New VM Instance (“Compute Engine”- Google Cloud).

Log in to Google Cloud Console, navigate to Compute Engine, and create a new VM instance, and Security Traffic & Cloud Key is taken default.
This instance will serve as your server.

![Create VM Instance on Google Cloud-Image](https://github.com/user-attachments/assets/f5b00ef1-fa92-4ed9-8676-782b1eab06e4)


Step 2:- Connect via SSH & Gain Root Access & Update Package Lists.

Use the SSH option in the Google Cloud Console to access your instance securely. This provides a command-line interface.
Run “sudo su”- to switch to the root user. This gives you administrative privileges needed for installations and configurations.
Execute “apt-get update”- to ensure your package lists are up-to-date, which is crucial for installing the latest software.

![Connect SHH-Image](https://github.com/user-attachments/assets/6f80ec8c-64e1-4932-a421-2b80779cf8d9)

![Root & Packages Update-Image](https://github.com/user-attachments/assets/9ac4cb9c-58fc-417b-99b0-70f22ebab940)


Step 3:- Install Apache2 & Check Apache Status.

Use “apt-get install apache2” - to install the Apache server, which will host your web application or static website.
Verify Apache is running by using - “systemctl status apache2” or “service apache2 status”. This ensures your server is active and ready.

![Installing Apache2-Image](https://github.com/user-attachments/assets/323e70f7-c8df-449e-b2ee-64437cd69a1d)

![Apache2 Status-Image](https://github.com/user-attachments/assets/48d627f9-270d-44f2-b06c-9e6b1d597fbd)


Step 4:-Create a Storage Bucket & Upload Files to the Bucket.

Navigate to the Cloud Storage page.
Click Create Bucket.
Set the Bucket name (must be globally unique).
Choose the Storage class and Location based on your needs.
Configure permissions (e.g., allow public or private access) & Click Create. 

![Bucket Created-Image](https://github.com/user-attachments/assets/4e476f4c-a7e9-4a3f-aa31-9eddadd07c31)

Go to your bucket.
Click Upload Files or Upload Folder.
Select the file(s) from your local machine and upload.

![Uploaded-Image](https://github.com/user-attachments/assets/1d4ddfa2-8a92-4762-ae90-8773fdd6139f)


Step 5:-Copy File from Cloud Storage to VM Instance.

Use the gsutil command to copy the file from the bucket to the VM:
--“gsutil cp gs://sachin-bg01/one-page-website/*  /var/www/html”
-sachin-bg01 with the name of storage bucket.
-one-page-website with the name of the uploaded file.
-/var/www/html with the destination directory on our VM instance.

![Copied to Bucket to VM Instance-Image](https://github.com/user-attachments/assets/e9b79a9d-e495-4c54-9e13-8a5e62ebba67)


Step 5:- OUTPUT - Deploy Static Web Application.

Copy the public IP address of your VM, open a browser, and navigate to it. Your application should now be running.


![Copied Public IP-Image](https://github.com/user-attachments/assets/e6945777-8ba2-413b-9671-6621566d024c)


![Pasted on browser-image](https://github.com/user-attachments/assets/593a9ec9-f2f0-4890-95c7-1ddedab90fb9)


![](https://github.com/user-attachments/assets/104d8cdc-879b-4d4c-b885-f7a0a1533517)


![Screenshot 2024-12-25 124402](https://github.com/user-attachments/assets/f86eaeb7-0935-4c44-85e4-98d76ae96d58)


![Screenshot 2024-12-25 124414](https://github.com/user-attachments/assets/85d26ba7-ae0a-4f78-ac47-8a8525a5a61a)


![Screenshot 2024-12-25 124436](https://github.com/user-attachments/assets/eceef70c-5465-4efb-bd98-f4abf5a7707f)


![Screenshot 2024-12-25 124504](https://github.com/user-attachments/assets/3230c715-cc81-425a-b513-917bbb467b12)


