
- Fundamentals of network security in AWS.
- Control traffic is allowed into or out of our EC2 instances
- Security groups only contain allow rules.
- Can only be referenced by IP or by Security Groups.
### Security Groups: Deeper Dive
- Security groups act as a firewall on EC2 Instances.
- They Regulate:
	- Access to ports.
	- Authorized IP ranges - IPv4 or IPv6
	- Control of inbound network (From other to instances)
	- Control of outbound network (From the instance to other)

![[Pasted image 20241113234952.png]]

## Security Group Diagram

![[Pasted image 20241113235443.png]]

1. Only one security group is present as shown in the diagram.
2. Only my computer which has authorized to access EC2 instance through security groups.
3. But the other computer which doesn't have port 22 authorized is not allowed to access the EC2 Instance.
4. EC2 instance allows any traffic out of it.

### Security Groups: Good to Know

- Can be attached to multiple instances.
- Locked down to a region / VPC combination i.e. if you change region you have to create a new security group or create another VPC
- Security groups live outside the EC2 instance that your instance cannot see the traffic blocked by the security groups.
- Its good to maintain one separate security group for SSH access.
- If your application is not accessible (time out), then its a security group issue.
- If your application gives a "connection refused" error then its an application error and application is not launched.
- All inbound traffic is blocked by default
- All outbound traffic is allowed by default.

### Referencing other security groups.

![[Pasted image 20241118234616.png]]

##### Explanation:

- As the diagram depicts there are total 4 instances which have attached security groups.
- The larger instance has Security group 1 
	- This have rules to allow inbound access of security group 1 and as well of security group 2
- Both the EC2 instances that have security group 1 and security group 2 attached are allowed regardless of there IP
- EC2 instance having security group 3 attached is not allowed even though having the same IP as first two instance because : The larger instance has Security group 1 which allows only inbound access to Instances which have Security group 1 and 2 attached hence not allowing Security group 3.


## Classic Ports to Know

- **22 = *SSH (Secure Shell)***  - Log into the Linux instance.
- **21 = *FTP (File Transfer Protocol)*** - upload files into the share files.
- **22 = *SFTP (Secure File Transfer Protocol)*** - uploads files using SSH.
- **80 = *HTTP*** - access unsecured websites.
- **443 = *HTTPS*** - access secured websites.
- **3389 = *RDP (Remote Desktop Protocol)*** - log into Windows instance.


## Security Groups Hand On.

- You can attach many security groups to a single instance.
- You can also attach the security group to another instance even if the security group is created in another instance.
- If you get any time out error with SSH or accessing the server or website from instance than that error is related to Security Groups definitely.