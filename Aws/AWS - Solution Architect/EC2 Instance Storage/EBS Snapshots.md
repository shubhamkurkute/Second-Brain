
- Make a backup (snapshot) of your EBS volume at a point in time
- Not necessary to detach volume to do snapshot, but recommended
- Can copy snapshots across AZ or Region

![[Pasted image 20241206233152.png]]


## EBS Snapshots Features

- **EBS Snapshot Archive**
	- Move a Snapshot to an "archive tier" that is 75% cheaper
	- Takes within 24 to 72 hours for restoring the archive
![[Pasted image 20241206233747.png]]
- **Recycle Bin for EBS Snapshots**
	- Setup rules to retain deleted snapshots so yo can recover them after an accidental deletion
	- Specify retention (from 1 day to 1 year)
![[Pasted image 20241206233803.png]]
- **Fast Snapshot Restore (FSR)**
	- Force full initialization of snapshot to have no latency on the first use ($)
	- This is uses more power to restore the snapshot 
	- As it is fast requires more money.