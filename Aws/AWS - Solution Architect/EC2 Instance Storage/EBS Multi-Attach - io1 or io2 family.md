
- Attach the same EBS volume to multiple EC2 instances in the same AZ 
- Each instance has full read and write permissions to the high performance volume
- Use case:
	- Achieve higher application availability in clustered Linux applications (ex : Teradata)
	- Applications must manage concurrent write operations
- Up to 16 EC2 instance at a time
- Must use a file system that cluster aware (not XFS, EXT4, etc..)
- ![[Pasted image 20241212173552.png]]


# EBS Encryption
- When you create an encrypted EBS volume, you get following
	- Data at rest is encrypted inside the volume 
	- All the data in flight moving between the instance and the volume is encrypted
	- All the snapshots are encrypted.
	- All the volumes created from encrypted snapshots are also encrypted.
	- Encryption and decryption are handled transparently (You have to do nothing about it)
	- Encryption has minimum impact on latency
	- EBS Encryption leverages keys from KMS (AES-256)
	- Copying an unencrypted snapshot allows encryption
	- Snapshots of encrypted volumes are encrypted

## Encryption : Encrypt an unencrypted EBS Volume
- Create an EBS snapshot of the volume
- Encrypt the EBS snapshot (using copy)
- Create a new EBS volume from the snapshot (The volume will also be encrypted)
- Now you can attach the encrypted volume to the original instance.