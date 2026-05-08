\# Linux for DevOps – Hands-on Learning Notes



\## Overview



This repository section contains practical Linux learning notes focused on DevOps, cloud infrastructure, troubleshooting, service management, networking, and operational workflows.



Learning Approach:



\* Learn

\* Practice

\* Break

\* Troubleshoot

\* Fix

\* Document



\---



\# Linux Basics



\## 1. Navigation \& File System Commands



\### Commands Practiced



```bash

pwd

ls

ls -l

ls -la

cd

mkdir

rmdir

touch

cp

mv

rm

find

```



\### Learning Outcome



\* Understood Linux directory structure

\* Practiced file and folder management

\* Learned absolute and relative paths

\* Worked with hidden files and directories



\---



\## 2. File Viewing \& Editing



\### Commands Practiced



```bash

cat

less

more

head

tail

nano

vim

```



\### Learning Outcome



\* Viewed and edited files from terminal

\* Monitored files and logs

\* Learned basic terminal-based editing



\---



\## 3. Permissions \& Ownership



\### Commands Practiced



```bash

chmod

chown

sudo

whoami

id

```



\### Learning Outcome



\* Understood file permissions

\* Practiced ownership management

\* Learned root vs normal user access

\* Troubleshooted permission denied issues



\---



\## 4. Process \& Service Management



\### Commands Practiced



```bash

ps aux

top

htop

kill

killall

systemctl

```



\### Service Commands



```bash

sudo systemctl start nginx

sudo systemctl stop nginx

sudo systemctl restart nginx

sudo systemctl status nginx

```



\### Learning Outcome



\* Monitored running processes

\* Managed Linux services

\* Practiced troubleshooting stopped services

\* Learned systemctl operations



\---



\## 5. Networking Commands



\### Commands Practiced



```bash

ping

curl

wget

ssh

scp

netstat

ss

ip a

nslookup

dig

```



\### Learning Outcome



\* Tested connectivity between systems

\* Learned SSH-based remote access

\* Checked open ports and network services

\* Understood basic DNS troubleshooting



\---



\## 6. Logs \& Troubleshooting



\### Commands Practiced



```bash

tail -f

journalctl

dmesg

cat

less

```



\### Important Location



```text

/var/log

```



\### Learning Outcome



\* Investigated service failures

\* Monitored logs in real time

\* Practiced troubleshooting using logs



\---



\## 7. Resource Monitoring



\### Commands Practiced



```bash

df -h

du -sh

free -m

uptime

vmstat

```



\### Learning Outcome



\* Monitored disk usage

\* Checked memory utilization

\* Understood basic system resource monitoring



\---



\# Advanced Linux Concepts



\## 1. Cron Jobs \& Automation



\### Commands Practiced



```bash

crontab -e

crontab -l

```



\### Learning Outcome



\* Learned task scheduling basics

\* Understood automation workflow



\---



\## 2. Bash Scripting



\### Concepts Practiced



\* Variables

\* Loops

\* Conditions

\* Functions

\* Exit codes



\### Example Scripts



\* Disk monitoring script

\* Service health check script

\* Backup automation script



\---



\## 3. Compression \& Archives



\### Commands Practiced



```bash

tar

zip

unzip

gzip

gunzip

```



\### Learning Outcome



\* Compressed and extracted files

\* Worked with archive management



\---



\## 4. Package Management



\### Ubuntu Commands



```bash

sudo apt update

sudo apt install

sudo apt remove

sudo apt upgrade

```



\### Learning Outcome



\* Installed and updated packages

\* Managed Linux software dependencies



\---



\# Real-World Troubleshooting Practice



\## Issues Practiced



\* SSH permission denied

\* Service not running

\* HTTP port blocked

\* Permission denied errors

\* Nginx troubleshooting

\* Security Group access issues

\* Linux file permission issues



\---



\# Practical DevOps Learning



\## Hands-on Environment



\* AWS EC2 Ubuntu Server

\* SSH Access

\* Linux Terminal Operations

\* Nginx Service Management



\---



\# Key Learning Outcome



Linux is not only about commands.

The main focus is:



\* Troubleshooting

\* Service management

\* Networking understanding

\* System monitoring

\* Operational confidence

\* Real-world debugging



This learning is being continued alongside AWS, Cloud, and DevOps hands-on practice.



