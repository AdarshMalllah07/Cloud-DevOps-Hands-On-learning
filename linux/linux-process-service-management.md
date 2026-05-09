Linux Hands-On — Process Management \& Service Management

Topics Covered

Process management

CPU \& memory monitoring

Background jobs

Killing processes

Service management

systemctl

nginx service handling

Logs \& troubleshooting

sudo \& chmod understanding

1\. Process Management

Purpose



Process management is used to:



monitor running applications

troubleshoot high CPU/memory usage

stop stuck processes

investigate application failures



Very important in:



DevOps

Cloud

Infrastructure Support

Production troubleshooting

Commands Practiced

ps aux

grep

top

htop

jobs

fg

kill

kill -9

free -m

df -h

du -sh

uptime

View Running Processes

ps aux

Understanding

Part	Meaning

ps	Process status

aux	Show all running processes

Important Columns

Column	Meaning

USER	Process owner

PID	Process ID

CPU	CPU usage

MEM	Memory usage

COMMAND	Running command

Find Specific Process

ps aux | grep nginx

Important Concept

|



called:



pipe



Sends output of one command into another.



Live Process Monitoring

top



Shows:



CPU usage

memory usage

load average

running processes



Exit:



q

Better Monitoring Tool



Install:



sudo apt install htop -y



Run:



htop



Used for:



cleaner monitoring

easier troubleshooting

process management



Exit:



q

Background Jobs



Run background process:



sleep 300 \&

Understanding

Symbol	Meaning

\&	Run in background

Check Background Jobs

jobs

Bring Job To Foreground

fg



Stop using:



CTRL + C

Kill Process



Find process:



ps aux | grep sleep



Kill process:



kill PID



Force kill:



kill -9 PID

Important Understanding

Command	Purpose

kill	Gracefully stop process

kill -9	Force terminate process

System Monitoring

Memory Usage

free -m

Disk Usage

df -h

Folder Size

du -sh \~/project

System Load

uptime



Used to understand:



server pressure

resource usage

performance issues

Real DevOps Usage



Process management is used for:



high CPU investigation

memory leak troubleshooting

stuck application debugging

deployment failures

production monitoring

2\. Service Management (systemd)

What Is systemctl?

Purpose



Manage Linux services through:



systemd

What Is systemd?



Linux service manager used to control:



nginx

docker

mysql

ssh

redis

applications

Important Commands

systemctl status nginx

systemctl start nginx

systemctl stop nginx

systemctl restart nginx

systemctl reload nginx

systemctl enable nginx

systemctl disable nginx

Check Service Status

systemctl status nginx



Look for:



active (running)

Start Service

sudo systemctl start nginx

Stop Service

sudo systemctl stop nginx

Restart Service

sudo systemctl restart nginx



Used after:



config changes

deployments

troubleshooting

Reload Service

sudo systemctl reload nginx

Difference

Command	Purpose

restart	full stop + start

reload	reload config without stopping

Enable Service On Boot

sudo systemctl enable nginx

Disable Auto Start

sudo systemctl disable nginx

Check Listening Ports

ss -tulnp



Used to check:



open ports

listening services

active applications

Nginx Logs



Go to:



cd /var/log/nginx



View logs:



cat error.log

tail -f error.log



Exit:



CTRL + C

journalctl



View service logs:



journalctl -u nginx



Live logs:



journalctl -u nginx -f

nginx Config Testing



Test config:



sudo nginx -t

Important Learning



Always test config before restart.



Wrong config can:



break application

cause downtime

fail deployment

Real DevOps Workflow

Service Down

→ Check Status

→ Check Logs

→ Check Ports

→ Test Config

→ Restart Service

→ Verify Application

3\. Important Command Definitions

sudo

Full Form

Super User DO

Purpose



Run command with:



root/admin privileges



Used for:



package installation

editing configs

restarting services

accessing protected directories

systemctl

Purpose



Manage Linux services using:



systemd



Used to:



start services

stop services

restart services

enable auto-start

troubleshoot applications

chmod

Full Form

Change Mode

Purpose



Change:



file/folder permissions



Examples:



chmod +x deploy.sh

chmod 755 deploy.sh

chmod 600 key.pem

Real DevOps Importance



These topics are heavily used in:



production troubleshooting

deployments

nginx management

cloud servers

CI/CD pipelines

Docker containers

monitoring systems

Real Learning Method

Learn

→ Practice

→ Break

→ Troubleshoot

→ Fix

