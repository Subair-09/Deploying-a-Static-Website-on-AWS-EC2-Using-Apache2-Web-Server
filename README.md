
# Deploying a Static Website on AWS EC2 Using Apache2  

![AWS](https://img.shields.io/badge/AWS-EC2-orange?logo=amazon-aws&style=for-the-badge)
![Apache](https://img.shields.io/badge/Web%20Server-Apache2-red?logo=apache&style=for-the-badge) 
![Linux](https://img.shields.io/badge/OS-Linux-yellow?logo=linux&style=for-the-badge)
![Template](https://img.shields.io/badge/Template-Free--CSS-green?style=for-the-badge)
![Educational](https://img.shields.io/badge/License-Educational%20Use-blue?style=for-the-badge)

A **step-by-step guide** to deploying a static website on an **AWS EC2** instance using **Apache2**. Perfect for DevOps beginners, cloud enthusiasts, or anyone looking to host a website on AWS!  

---

## 📌 Table of Contents  
- [Features](#-features)  
- [Template Source](#-template-source)  
- [Prerequisites](#-prerequisites)  
- [Quick Deployment](#-quick-deployment)   
- [Author](#-Author)  
- [License](#-license)  

---
## ✨ Features  
**Full AWS EC2 Setup** – Launch & configure an EC2 instance  
**Apache2 Installation** – Set up a secure & efficient web server  
**Static Website Hosting** – Deploy HTML/CSS/JS files  
**Security Best Practices** – Configure security groups & SSH access  

 ---
 
## 🌐 Template Source  
The website template used in this project is from **[Free-CSS](https://www.free-css.com/)**:  
- Free to use for personal and educational projects  
- Responsive design works on all devices  
- Clean HTML/CSS structure for easy modification  

---
## 🛠 Prerequisites  
Before you begin, ensure you have:  
- An **[AWS account](https://aws.amazon.com/)** (Free Tier eligible)  
- Basic **Linux command-line** knowledge   
- Static website files (HTML/CSS/JS)  

🔗 *Need help creating an EC2 instance?*  
Check out my step-by-step guide:  
[**Creating an EC2 Instance in AWS - A Step-by-Step Guide**](https://nucloud.hashnode.dev/creating-an-ec2-instance-in-aws-a-step-by-step-guide)  

---
## 🚀 Quick Deployment  

### Set Up an AWS Linux VM (EC2 Instance)
Launch an EC2 instance using Amazon Linux or Ubuntu.

Configure security groups to allow SSH (port 22) and HTTP (port 80) traffic.

Connect to the instance using SSH and your .PEM key file.

To learn more about how to create an EC2 instance in AWS. You can also check out my previous article Here on creating an EC2 instance in AWS for a step-by-step guide.

### Connect to the EC2 Instance
**1.**. Use the **ls** command to list the contents of your home directory to confirm the Downloads folder exists

**2.**. You should see a folder named Downloads.

**3.**. Get into the Downloads folder using the **Cd** command

**4**. For security reasons, the **.Pem** key file have restricted permissions. Run the **Chmod 400** command to set the correct permissions:
The **Chmod 400** command is used to set file permissions so that the file is read-only for the owner and no permissions for others. This is a security best practice for **.Pem** key files used to connect to EC2 instances.

**5**. Run **ssh** command to connect to your EC2 instance, Once you SSH into the EC2 instance, your terminal session is connected to the remote server, not your local machine. Any commands you run will execute on the remote server, not your local computer. The terminal prompt will reflect the remote server's hostname or IP address. i.e. **ubuntu@ip-172-31-21-194.**
**6**. **Run sudo apt update -y** command to refresh the list of available packages and their versions from the repositories configured on your system.

**7**. Install apache2 using the command **sudo apt install apache2**

**8**. Change to the default Apache document root directory by using **cd /var/www/html** Check the contents of the directory **/var/www/html** by using the command **ls** to list and conform the **index.html** file that populate the apache webserver default page.

**9**. use the **sudo rm -rf** to delete the index.html file that populate the default page of apache2 webserver and use the ls command to confirm deletion

**10**. Now that we are inside the Apache webserver directory /var/www/html, we need too download and replace our static website template files into this directory using the command **wget** followed by the download link to our static website.

**11.**. Now that we have downloaded our template using **wget**, and since the file is a zip file, we need to install the unzip utility on Ubuntu. Use the command **sudo apt install unzip** to do this and use the command **sudo apt unzip** to unzip our template folder.

**12.**. Use the **ls** command to list the contents of our folder that was downloaded into **/var/www/html.**

**13.**  Use the cd command to enter the **handtime-html**directory, and then use the **ls** command to list all the files and folders that make up our static website, such as **about.html, contact.html, index.html,** and so on.

**14.** Navigate to the EC2 Dashboard and Copy the **Public DNS Address**, The **Public IPv4 DNS** look like this **ec2-13-61-44-14-eu-North-1.compute.amazonaws.com....**.

**15**  Navigate to your browser and paste the **Public DNS Address** to display our static website.

### Author  

**Subair Nurudeen Adewale**  
[![LinkedIn](https://img.shields.io/badge/-LinkedIn-blue?style=flat&logo=linkedin)](https://www.linkedin.com/in/subair-nurudeen-adewale-1b46aa28b/) 
[![Hashnode](https://img.shields.io/badge/-Hashnode-2962FF?style=flat&logo=hashnode)](https://nucloud.hashnode.dev)  

### 🛠️ Technical Expertise  
- **Cloud DevOps Engineer** (AWS | CI/CD | IaC)  
- **IT Telecom Support Technician**  
- **Application Security Tester** (OWASP | PenTesting)
- **Co-Founder Codespehere Academy**

### 📫 Let's Connect  
- Blog: [NuCloud on Hashnode](https://nucloud.hashnode.dev)    
- Email:Nuddywale@gmail.com  

---
## 📜 Educational License

This project and all associated materials are licensed **for educational purposes only**.







