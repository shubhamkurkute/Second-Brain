
## Elastic Block Storage
- **EBS Volumes...**
	- one instance except io1 and io2 which supports EBS multi attach
	- Are locked i.e. specific to Availability Zone (AZ) level
	- gp2 : IO increases if disk size increases
	- gp3 and io 1 : can increase IO independently
- To migrate an EBS volume across AZ
	- Take a snapshot
	- Restore the snapshot to another AZ
	- EBS backups use IO and you shouldn't run them while your application is handling a lot of traffic.
- Root EBS volumes of instances get terminated by default if the EC2 instance gets terminated. (you can also disable it)
![[Pasted image 20241213001258.png]]

## Elastic Network Storage
- **EFS Volumes...**
	- Mounting 100s of instances across AZ
	- EFS share website files (WordPress)
	- Only for Linux Instances (POSIX)
	- EFS has higher price point than EBS
	- Can leverage Storage Tiers for cost savings
	- Remember: EFS vs EBS vs Instance Store
![[Pasted image 20241213001311.png]]