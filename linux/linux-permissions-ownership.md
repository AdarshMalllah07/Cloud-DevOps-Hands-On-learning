Linux Hands-On — Permissions \& Ownership

Topics Covered

Linux permissions

File ownership

Execute permissions

chmod

sudo

Script execution

Numeric permissions

1\. Understanding File Permissions

Commands Practiced

ls -l

whoami

id

Example Permission Output

\-rw-rw-r-- 1 ubuntu ubuntu permissions.txt

Permission Breakdown

Part	Meaning

\-	File

rw-	Owner permissions

rw-	Group permissions

r--	Others permissions

Permission Symbols

Symbol	Meaning

r	Read

w	Write

x	Execute

Important Learning

Linux permissions are strict

Permission issues are very common in DevOps

Scripts require execute permission

Root user has highest privileges

2\. User \& Group Information

Current User

whoami



Expected:



ubuntu

User \& Group Details

id



Used to check:



user ID

groups

permission context

3\. Removing Write Permission

Command

chmod -w permissions.txt

Verify Permissions

ls -l

Test Write Operation

echo "Testing permissions" >> permissions.txt



Expected:



Permission denied

Learning



Removing write permission prevents file modification.



Real-world DevOps usage:



protecting configs

restricting access

securing deployment files

4\. Restoring Write Permission

Command

chmod +w permissions.txt

Append Data Again

echo "Permissions fixed" >> permissions.txt

Read File

cat permissions.txt

Important chmod Commands

Command	Meaning

chmod +w	Add write permission

chmod -w	Remove write permission

chmod +x	Add execute permission

5\. Script Execution Permissions

Create Script

touch deploy.sh

Add Script Content

echo 'echo "Deployment Running"' > deploy.sh

Try Running Script

./deploy.sh



Expected:



Permission denied

Learning



Scripts need execute permission before running.



Add Execute Permission

chmod +x deploy.sh

Run Script Again

./deploy.sh



Expected:



Deployment Running

Real DevOps Importance



Execute permissions are required for:



deployment scripts

automation

CI/CD pipelines

shell scripts

6\. Numeric Permissions

Command

chmod 777 permissions.txt

Verify

ls -l



Expected:



rwxrwxrwx

Numeric Permission Table

Number	Meaning

7	rwx

6	rw-

5	r-x

4	r--

Important Warning



Avoid:



chmod 777



in production unless absolutely necessary.



Reason:



gives full access to everyone

security risk

Common Safe Permissions

Permission	Usage

755	Scripts/directories

644	Config files

600	Private keys

7\. sudo \& Root Privileges

Create File In Protected Location

sudo touch /var/log/devops.log

Verify

ls -l /var/log/devops.log

Learning



Some Linux directories require:



root access

elevated privileges



Used constantly in:



package installation

service management

log handling

configuration changes

Important DevOps Understanding



Permissions are involved in:



nginx failures

Docker volume issues

deployment failures

SSH key problems

CI/CD pipeline errors

application startup failures

