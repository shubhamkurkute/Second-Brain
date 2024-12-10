
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
	- Max PIOPS: 64K for Nitro EC2 instances and  