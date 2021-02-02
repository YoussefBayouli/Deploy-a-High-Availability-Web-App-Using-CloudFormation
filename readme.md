# Deploy a High-Availability Web App using CloudFormation

In this project (Udagram App), I deployed web servers for a highly available web app using CloudFormation. I wrote the script that creates and deploys the infrastructure and application for an Udagram app from the ground up. The script begin deploying the networking components followed by servers, security roles and software.

![high availability webapp architecture diagram](https://user-images.githubusercontent.com/75679079/106497682-a6cdc880-64be-11eb-9760-7b5369a9c1af.png)


# Files included 
	* Udagram App : Udagram App Code (Bootssrap CSS framework, Font, and JavaScript libraries needed for the website to function etc ...)
	* Create.sh : Cloudformation create stack script. 
	* Update.sh : Cloudformation update stack script.
	* UdagramApp.yml: Udagram Project's CloudFormation script.
	* UdagramServers.json : Udagram Project's CloudFormation script parameters. 
	* Images-of-result-deploy : Screenshot the result of deploy.



# Connecting to an ec2 instance in a private subnet on AWS : 

In this project i used a bastion host in order to connect to the instances (for troubleshooting) in the private subnet , 
for that i used SSH agent forwarding , which allows me to connect from the bastion to the other instances 
without storing the private key on the bastion which is a very bad practice . 
The SSH agent is a program that keeps track of the user identity keys .For the deployement part  please find config file

# Config file : 
The SSH config file is a great resource for storing all the configuration for the remote machines you connect to. It is located in home directory .ssh/config.

	Host bastion-instance
	   HostName <Bastion Public IP>
	   User ubuntu
	Host private-instance
	   HostName <Private IP>
	   User ubuntu
	   ProxyCommand ssh -q -W %h:%p bastion-instance

