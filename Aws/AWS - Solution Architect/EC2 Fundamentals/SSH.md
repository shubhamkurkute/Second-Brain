
# SSH Summary Table

![[Pasted image 20241121234312.png]]

- This Image depicts that SSH cannot be used below windows 10.
- SSH is a command line application.
- Putty can be used to run EC2 instance on O.S. below windows 10.
- EC2 connect is a web application and supports all the O.S.

## SSH into EC2 instance using Linux/ Mac OS X

- SSH is a tool that allows you to control a remote machine, all using the command line.
- To get into the EC2 instance we require .pem we downloaded after creation of instance.
- This .pem file should be in same directory from where the cmd is launched.
- Command for launching the EC2 instance is:
	`ssh -i EC2Tutorial.pem ec2-user@public-ip-of-instance`

## SSH into EC2 using Windows using PUTTY

- In this we use Putty in order launch EC2 instance on the windows
- First create .ppk using a .pem from Putty gen application.
- After that enter host name as ec2-user@public-ip-of-instance.
- Later direct to SSH -> Auth->credentials and browse for the .ppk file in private key file authentication.
- At last launch the session.

## SSH into EC2 using Windows CMD.

- Same command as the Linux/ mac but if have issue for permissions then steps to follow:
	1. Go to file and right click -> properties -> Security -> advanced
	2. Disable inheritance then click Add.
	3.  Select principal your name and then apply.


## EC2 Roles

- Don't use aws configure command as any one can get our credentials from this instance
- Never enter your aws access key and secret key into EC2 instance.
- We can use roles to allow aws services into the instance rather than configuring aws.