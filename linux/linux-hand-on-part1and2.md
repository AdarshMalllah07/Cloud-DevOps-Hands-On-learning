Linux Hands-On Notes — Part 1 \& 2

Topics Covered

Navigation \& File System

File Operations

Paths

Logs

Basic Linux Workflow

1\. Navigation \& File System

Commands Practiced

pwd

ls

ls -l

ls -la

cd

mkdir

touch

tree

Important Linux Directories

Directory	Purpose

/	Root directory

/home	User home directories

/home/ubuntu	Ubuntu user home

/etc	Configuration files

/var/log	System \& application logs

/tmp	Temporary files

Important Concepts

Absolute Path



Full path from root.



Example:



/home/ubuntu/project

Relative Path



Path from current location.



Example:



cd project

Hidden Files



Files starting with:



.



Example:



.bashrc

.profile



Show hidden files:



ls -la

Mistakes \& Learning

Wrong Path Example

cd /log



Error:



No such file or directory



Correct path:



cd /var/log



Learning:



/log and /var/log are different

Linux paths are strict

2\. File Operations

Commands Practiced

touch

cat

head

tail

cp

mv

rm

less

File Creation



Create files:



touch app.log

touch nginx.conf

touch deploy.sh

Add Content To File



Overwrite file:



echo "Hello DevOps" > app.log



Append to file:



echo "Linux Practice" >> app.log

Important Operators

Symbol	Meaning

>	Overwrite file

>>	Append to file

Read File Content

cat app.log

View First Lines

head app.log

View Last Lines

tail app.log

Copy Files

cp nginx.conf nginx.conf.backup



Real DevOps usage:



backup config before changes

Rename Files

mv deploy.sh deploy-script.sh

Create Folders

mkdir logs configs scripts

Move Files

mv app.log logs/

mv nginx.conf configs/

mv deploy-script.sh scripts/

View Folder Structure

tree



OR



ls -R

Wildcards



Copy all .log files:



cp \*.log backup-logs/

Important Concept

\*



means:



match everything



Example:



\*.log



means:



all .log files

Delete Files

rm error.log

Logs \& Monitoring



Read large file:



less /var/log/syslog



Exit:



q

Monitor Logs Live

tail -f /var/log/syslog



Exit:



CTRL + C

Important Learning



Linux learning should follow:



Learn

→ Practice

→ Break

→ Troubleshoot

→ Fix

Real DevOps Understanding



Commands practiced are heavily used in:



logs

deployments

nginx configs

monitoring

troubleshooting

automation

cloud servers

