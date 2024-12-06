
## What's an EBS Volume?

1. An EBS Volume is a network drive you can attach to your instances while they run.
2. It allows instance to persist data even after the termination i.e. data is preserved even if instance is terminated and this volume can be mounted to another instance.
3. They can only be mount to one instance at a time.
4. They are bound to specific availability zone
5. Its a network drive
	1. It uses the network to communicate the instance, which means there might be a bit of latency
	2. It can be detached from an EC2 instance and attached to another one quickly
6. Its locked to an Availability Zone (AZ)
	1. An EBS Volume in us-east-1 a cannot be attached to us-east-1 b
	2. To move a volume across, you first need to snapshot it.
7. Have a provisioned capacity (size in GBs and IOPS (Input output per second))
	1. You get billed for all the provisioned capacity
	2. You can increase the capacity of the drive over time.

## Example

![[Pasted image 20241205233843.png]]

 