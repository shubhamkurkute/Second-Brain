- EFS Scale
	- 1000s of concurrent NFS clients, 10 GB+ /s throughput
	- Grow to Petabyte-scale network file system, automatically
- Performance Mode (set at EFS creation time)
	- General Purpose (default) - latency -sensitive use cases (web-server, CMS, etc..)
	- Max I/O - higher latency, throughput, highly parallel (big data, media processing)
- Throughput Mode:
	- Bursting - 1TB = 500MiB/s + burst up to 100MiB/s
	- Provisioned - set your throughput regardless of storage size, ex: 1 GiB/s for 1TB storage
	- Elastic - automatically scales throughput up or down based on your workloads
		- up to 3GiB/s for reads and 1GiB/s for writes
		- Used for unpredictable workloads

## EFS - Storage classes
- Storage Tiers (lifecycle management feature - move file after N days)
	- Standard : for frequently accessed files
	- Infrequent access (EFS-IA): cost to retrieve files, lower price to store.
	- Archive: rarely accessed data (few times each year), 50% cheaper
	- Implement lifecycle policies to move files between storage tiers
- Availability and durability
	- Standard: Multi-AZ, great for prod
	- One Zone: One AZ, great for dev, backup enabled by default, compatible with IA (EFS One Zone IA)
- Over 90% in cost savings.

![[Pasted image 20241213000332.png]]