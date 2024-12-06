
- AMI = Amazon Machine Image
- AMI are a customization of an EC2 instance
	- You add your own software, configuration, operating system, monitoring...
	- Faster boot / configuration time because all your software is pre-packaged
- AMI are built for a specific region (and can be copied across regions)
- You can launch EC2 instances from:
	- A public AMI: AWS provided
	- Your own AMI: You make and maintain them yourself
	- An AWS marketplace AMI: an AMI someone else made (and potentially sells)


## AMI Process (From an EC2 Instance)

- Start an EC2 instance and customize it
- Stop the instance (for the data integrity)
- Build an AMI - this will also create EBS snapshots
- Launch instances from other AMIs

![[Pasted image 20241207000554.png]]