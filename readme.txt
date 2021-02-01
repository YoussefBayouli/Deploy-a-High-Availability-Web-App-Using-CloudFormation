![alt text](https://github.com/[YoussefBayouli]/[Deploy-a-High-Availability-Web-App-Using-CloudFormation]/blob/[master]/image.jpg?raw=true)


Please find attached : 
	
	*UdagramApp.yml: Udagram Project's CloudFormation script.
	*UdagramServers.json : Udagram Project's CloudFormation script parameters. 
	*/Images-of-result-deploy : Screenshot the result of deploy.
	* /App of Udagram : Udagram App Code (Bootssrap CSS framework, Font, and JavaScript libraries needed for the website to function etc ...)
	* create.sh : Cloudformation create stack script. 
	* update.sh : Cloudformation update stack script.


						
*In this project i used a bastion host in order to connect to the instances (for troubleshooting) in the private subnet , 
for that i used SSH agent forwarding , which allows me to connect from the bastion to the other instances 
without storing the private key on the bastion which is a very bad practice . 
The SSH agent is a program that keeps track of the user identity keys .For the deployement part  ,please find config file

