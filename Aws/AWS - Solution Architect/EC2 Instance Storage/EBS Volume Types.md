
## General Purpose SSD
- Cost effective storage, low-latency
- System boot volumes, Virtual desktops, Development and test environments 
- 1 GiB - 16 TiB
- gp3:
	- Baseline of 3k IOPS and throughput of 125 MiB/s
	- Can increase IOPS up to 16000 and throughput up to 1000 MiBs independently
- gp2:
	- Small gp2 volumes can burst IOPS to 3k
	- Size of the volume and IOPS are line, max IOPS is 16k
	- 3 IOPS per GB, means at 5334 GB we are at the max IOPS

## Provisioned IOPS (PIOPS) SSD
- Critical business applications with sustained IOPS performance
- Or applications that need more than 16K IOPS
- Great for databases workloads (sensitive to storage perf and consistency)
- io 1 (4 GiB - 16 TiB):
	- Max PIOPS: 64K for Nitro EC2 instances and  32K  for other
	- Can increase PIOPs independently from storage size
- io 2 Block Express (4 GiB - 64 TiB)
	- Sub-millisecond latency
	- Max PIOPs : 256K with an IOPS: GiB ratio of 1000:1
- Supports EBS multi-attach

## Hard Disk Drives (HDD)
- Cannot be a boot volume 
- 125 GiB to 16 TiB
- Throughput Optimized HDD (st1)
	- Big data, Data Warehouses, Log processing
	- Max throughput 500 MiB/s - max IOPS 500
- Cold HDD (sc1)
	- For the data that is frequently accessed
	- Scenarios where lowest cost is important
	- Max throughput 250 MiB/s - max IOPS 250

# EBS Volume Summary

![[Pasted image 20241212172237.png]]


![[Pasted image 20241212172256.png]]