
- Managed NFS (network file system) that can be mounted on many EC2
- EFS works with EC2 instance in multi-AZ
- Highly available, scalable, expensive (3x gp2), pay per use

![[Pasted image 20241212180655.png]]

- Use cases: content management, web serving, data sharing, WordPress
- Uses NFSv4.1 protocol
- Uses security groups to control access to EFS
- Compatible with Linux AMI (not Windows)
- Encryption at rest using KMS
- POSIX file system (~Linux) that has a standard file API
- File system scales automatically, pay-per-use, no capacity planning.