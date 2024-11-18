

## Important points to remember to launch Instances


1. Instance types differ in no. of CPU's, how much memory they have and costing.
2. Creating a key-pair is mandatory to login using SSH.
3. Key pair type should be RSH type.
4. Private key file format:
	1. .pem : If you are using mac, Linux or windows 10 or higher. This is used with SSH.
	2. .ppk: If you have window lesser than 10 than use this. This is used with putty.
5. Security group attached to the instance controls the traffic in and out.
6. Instance gets public IP.
7. User data in advanced section is to add script to run it only on first launch.
8. Instance has a unique Instance ID.
9. Public IPv4 address is used to access our instance.
10. There is also a private IPv4 which is used to access instance internally on AWS which is private.
11. Longer you keep running instance more you pay, once you stop AWS don't charge for it.
12. Public IP keep on changing whenever you try running the instance after stopping it.
13. But private IP remains the same even after re-running the instance.