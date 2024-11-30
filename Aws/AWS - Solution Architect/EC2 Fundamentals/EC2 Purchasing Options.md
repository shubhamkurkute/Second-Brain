
## Types of EC2 purchasing options.

1. **On-Demand Instances** - short workload, predictable pricing, pay by second. Instance that we have created is of this type.
2. Reserved (1 and 3 years) : 
	1.  Reserved Instances : long workloads
	2. Convertible Reserved Instances: long workload with flexible instances i.e. can change type of instance.
3. Savings plan (1 and 3 years): These instances are to be used only within a particular amount, also can be used for long workloads.
4. Spot Instances: This instances are used for short workload and are cheap but user can lose instance if higher amount is paid by another user.
5. Dedicated Host: Book an entire physical server, control instance placement.
6. Dedicated Instances : No other customer will share your hardware.
7. Capacity Reservations : Reserve capacity in a specific AZ for any duration

### On Demand Instances:

1. Pay for what you use:
	1. Linux or windows: Billing per second, After you use.
	2. All other O.S. : Billing per hour.
2. Has the highest cost but no upfront payment
3. No long term commitment
4. Recommend for short-term and un-interrupted workloads, where you can't predict how the application will behave.


### Reserved Instances:

1. Up to 72% discount which may change according to time compared to On demand.
2. You reserve a specific instance attributes (Instance Type, Region, Tenancy, OS)
3. Reservation period - 1 year(+ discount) or 3 years (+++discount)
4. Payment options - upfront(+), partially upfront(++), All upfront(+++)
5. Reserved Instance's Scope - Regional or Zonal (reserve capacity in AZ)
6. Recommend for steady-state usage applications (think database)
7. You can buy or sell in the Reserved instance marketplace
8. Convertible Reserved Instance:
	1. Can change the EC2 instance type, instance family ,OS, scope, tenancy
	2. Up to 66% discount


### Saving Instances

1. Get a discount on long term usage up to 72% same as reserved instances.
2. Commit to certain type of usage ($10/hour for 1 or 3 years).
3. Usage beyond EC2 savings plans is billed at the On-Demand price.
4. Locked to a specific instance family and AWS region for e.g. M5 in us-east-1
5. Flexible across:
	1. Instance Size (e.g. m5.large, m5.2xlarge)
	2. OS(Linux, Windows)
		1. Tenancy (Host, Dedicated, Default)


### Spot Instances

1. Can get a discount of up to 90% compared to On demand
2. Instances that you can 'lose' at any point of time if your max price is less than the current spot price.
3. The MOST cost-efficient instances in AWS
4. Useful for workloads that are resilient to failure
	1. Batch jobs
	2. Data Analysis
	3. Image processing
	4. Any distributed workloads
	5. Workloads with a flexible star and end time
5. Not suitable for critical jobs or databases


### Dedicated Host

1. A physical server with EC2 instance capacity fully dedicated to your use
2. Allows you address compliance requirements and use your existing server bound software licenses (per-socket, per-core, per-VM software licenses)
3. Purchasing Options:
	1. On demand: Pay per second for active Dedicated Host
	2. Reserved- 1 or 3 years (No Upfront, Partial, All)
4. The most expensive option
5. Useful for software that have complicated licensing model (BYOL - Bring your own license)
6. Or for companies that have strong regulatory or compliance needs


### Dedicated Instances

1. Instances run on hardware that's dedicated to you.
2. May share hardware with other instances in same account
3. No control over instance placement (can move hardware after Stop/Start)
4. ![[Pasted image 20241201014317.png]]


### Capacity Reservations

1. Reserve On-Demand instances capacity in a specific AZ for any duration
2. You always have access to EC2 capacity when you need it.
3. No time commitment (create/cancel anytime). no billing discounts
4. Combine with Regional Reserved Instances and Savings Plans to benefit from billing discounts
5. You're charged at On-demand rate whether you run instances or not
6. Suitable for short term uninterrupted workloads that needs to be in a specific AZ