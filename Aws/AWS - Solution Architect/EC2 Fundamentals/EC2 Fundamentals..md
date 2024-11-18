
-  EC2 is one of the popular offering from Amazon.
-  EC2 = Elastic Compute Cloud = Infrastructure as Service.
-  It mainly consists of :
	- Renting virtual machines(EC2)
	- Storing data on virtual devices(EBS: Elastic Block Storage)
	- Distributing load across machines(ELB: Elastic Load Balancing)
	- Scaling the services using auto-scaling group(ASG: Auto Scaling Group)
- EC2 offers OS; Windows, Linux and MacOS
- Offers compute power and cores (CPU)
- Offers RAM
- Storage space:
	- Network Attached (EBS and EFS: Elastic File System)
	- Hardware (EC2 Instance Store)
- Network Card: Speed of the card, Public IP address
- Firewall Rules: Security group
- Naming Convention for EC2:
	- m5.2xlarge
	- m = Instance class
	- 5 = generation
	- 2xlarge = size of the instance i.e. more the size more the memory more the CPU on the instance.


## EC2 User Data

- It is possible to bootstrap our instances using an EC2 User data script.
- Bootstrapping means launching commands when machine starts.
- That script is only run once at the instance first start
- EC2 user data is used to automate boot tasks such as:
	- Installing updates
	- Installing software
	- Downloading common files from the internet 
	- Anything you can think of
- The EC2 user data scripts run with the root user i.e. sudo before any command
- Longer the Data script longer time it will take to boot instance.
