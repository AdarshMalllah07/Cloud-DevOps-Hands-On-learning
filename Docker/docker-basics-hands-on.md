\# Docker Basics Hands-On



\## Docker Installation



```bash

docker --version



Verify Docker installation.



First Docker Container

docker run hello-world

Understanding

Downloads image from Docker Hub

Creates container

Runs container

Prints output

Exits automatically

Docker Images

docker images



Shows downloaded local images.



Learned

Image = blueprint/template

Example:

nginx

ubuntu

hello-world

Docker Containers

Running Containers

docker ps

All Containers

docker ps -a

Learned

Container = running instance of image

Containers can be:

running

stopped

exited

Ubuntu Interactive Container

docker run -it ubuntu

Learned

\-i = interactive

\-t = terminal

Entered isolated container shell



Commands practiced:



pwd

ls

hostname

cat /etc/os-release



Exit container:



exit

nginx Container

docker run --name mynginx -d -p 8080:80 nginx

Learned

\--name = custom container name

\-d = detached/background mode

\-p = port mapping



Port Mapping:



Host Port 8080

→ Container Port 80



Traffic Flow:



Browser

→ localhost:8080

→ nginx container

→ nginx service

Docker Logs

docker logs mynginx



Used for troubleshooting containers.



Docker Exec

docker exec -it mynginx bash

Learned

Enter inside running container

Useful for debugging/troubleshooting

Container Management

Stop Container

docker stop mynginx

Start Container

docker start mynginx

Remove Container

docker rm mynginx

Image Removal

docker rmi nginx

Learned

Images cannot be removed while containers still reference them

Must:

stop container

remove container

remove image



Force remove:



docker rmi -f nginx

Cleanup



Remove stopped containers:



docker container prune

Important Concepts Learned

Concept	Meaning

Image	blueprint/template

Container	running instance

Docker Hub	image registry

Port Mapping	expose container externally

Logs	troubleshooting

Exec	access running container

Key Understanding



Docker provides consistent and portable application environments for modern DevOps and Cloud workflows.

