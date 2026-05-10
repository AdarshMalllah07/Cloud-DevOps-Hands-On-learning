Linux Hands-On — Remaining Important Linux Topics

Topics Covered

Package Management

Cron Jobs \& Automation

Environment Variables

Compression \& Archives

Disk \& Storage

SSH Basics

Bash Scripting

Nginx Basics

Linux Automation Concepts

1\. Package Management

Purpose



Install, update, and remove software packages in Linux.



Used constantly for:



nginx

docker

git

monitoring tools

cloud utilities

Ubuntu/Debian Commands

sudo apt update

sudo apt install nginx

sudo apt remove nginx

sudo apt upgrade

Important Understanding

Command	Purpose

apt update	refresh package list

apt install	install software

apt remove	uninstall software

apt upgrade	update installed packages

Real DevOps Usage



Used during:



server setup

deployments

tool installation

maintenance

2\. Cron Jobs \& Automation

Purpose



Run tasks automatically at scheduled times.



Edit Cron Jobs

crontab -e

View Cron Jobs

crontab -l

Example Cron Job

\* \* \* \* \* echo "Hello DevOps" >> /tmp/test.log



Runs every minute.



Real Usage



Used for:



backups

monitoring

cleanup

automation scripts

3\. Environment Variables

Purpose



Store reusable values for applications and system configuration.



View Variables

env

Create Variable

export NAME="Ganesh"

Use Variable

echo $NAME

Important Variable

echo $PATH



Shows executable search paths.



Real DevOps Usage



Environment variables are heavily used in:



Docker

CI/CD

applications

cloud configuration

4\. Compression \& Archives

Purpose



Compress and archive files/folders.



Used for:



backups

deployments

log storage

file transfer

tar Commands

Create Archive

tar -cvf backup.tar project/

Extract Archive

tar -xvf backup.tar

gzip Commands

gzip file.txt

gunzip file.txt.gz

zip Commands

zip backup.zip file.txt

unzip backup.zip

5\. Disk \& Storage

Important Commands

lsblk

df -h

du -sh

mount

umount

Purpose

Command	Purpose

lsblk	show disks

df -h	disk usage

du -sh	folder size

mount	attach storage

umount	detach storage

Real DevOps Usage



Used for:



AWS EBS volumes

storage troubleshooting

disk full investigation

6\. SSH Basics

SSH Connection

ssh -i key.pem ubuntu@IP

Copy File To Server

scp -i key.pem file.txt ubuntu@IP:/home/ubuntu

Generate SSH Key

ssh-keygen

Common SSH Issues

Problem	Cause

Permission denied	wrong key/user

Key not accessible	wrong path

Connection timeout	SG/firewall issue

Bad permissions	PEM permissions issue

Important Learning



SSH uses:



public/private key authentication

known\_hosts verification

secure remote access



Core cloud/devops skill.



7\. Bash Scripting

Purpose



Automate Linux tasks.



Used for:



monitoring

backups

deployments

cleanup

CI/CD automation

Create Script

nano first-script.sh

Example Script

\#!/bin/bash



echo "Hello DevOps"

Make Executable

chmod +x first-script.sh

Run Script

./first-script.sh

Variables

NAME="Ganesh"



echo $NAME

User Input

read NAME

Conditions

if \[ $NUMBER -gt 5 ]

then

&#x20;   echo "Greater"

fi

Loops

for i in 1 2 3

do

&#x20;   echo $i

done

File Check

if \[ -f /etc/nginx/nginx.conf ]

then

&#x20;   echo "File Exists"

fi

Important Bash Concepts

Concept	Purpose

Variables	store values

if	conditions

loops	repetition

read	user input

chmod +x	execute permission

Real DevOps Usage



Scripts used for:



server monitoring

deployment automation

health checks

cleanup jobs

backups

8\. Nginx Basics

Test Config

sudo nginx -t

Restart nginx

sudo systemctl restart nginx

Nginx Logs

/var/log/nginx/access.log

/var/log/nginx/error.log

Real Usage



Nginx commonly used for:



reverse proxy

frontend hosting

API routing

web serving

Most Important Linux Commands Learned

ls

cd

pwd

mkdir

touch

cp

mv

rm

cat

tail -f

grep

chmod

sudo

ps aux

top

kill

systemctl

journalctl

df -h

free -m

ip a

ping

curl

ssh

scp

crontab

tar

