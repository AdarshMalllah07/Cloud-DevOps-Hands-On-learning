\# EC2 Nginx Setup



\## Objective

Launch Ubuntu EC2 instance and host a simple web page using Nginx.



\---



\# Services Used

\- EC2

\- Security Groups

\- User Data



\---



\# EC2 Configuration



| Setting | Value |

|---|---|

| AMI | Ubuntu |

| Instance Type | t2.micro |

| Security Group | SSH + HTTP |

| Authentication | PEM Key |



\---



\# User Data Script



```bash

\#!/bin/bash



apt update -y

apt install nginx -y



systemctl enable nginx

systemctl start nginx



echo "<h1>AWS EC2 Nginx Server Running</h1>" > /var/www/html/index.html

```



\---



\# Steps Performed



\## 1. Created EC2 Instance

Configured Ubuntu server with public IP.



\### Screenshot

!\[EC2 Running](../screenshots/ec2-instance-running.png)



\---



\## 2. Configured Security Group



Allowed:

\- SSH Port 22

\- HTTP Port 80



\### Screenshot

!\[Security Group](../screenshots/security-group.png)



\---



\## 3. Connected Using SSH



```bash

ssh -i EC2Setup.pem ubuntu@<public-ip>

```



\### Screenshot

!\[SSH Connected](../screenshots/ssh-connected.png)



\---



\## 4. Verified Nginx



```bash

sudo systemctl status nginx

```



\---



\## 5. Verified Browser Access



Accessed:

```text

http://<public-ip>

```



\### Screenshot

!\[Nginx Browser](../screenshots/nginx-browser-output.png)



\---



\# Issues Faced



\## SSH Key Permission Error



\### Error

```text

Permissions for 'EC2Setup.pem' are too open.

```



\### Fix

Updated PEM file permissions in Windows Security Settings.



\---



\# Learning Outcome



\- Learned EC2 setup

\- Practiced SSH connectivity

\- Understood Security Groups

\- Learned User Data usage

\- Practiced Linux service management

\- Troubleshooted SSH permission issue

