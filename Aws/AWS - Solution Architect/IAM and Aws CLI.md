
## IAM Introduction: Users and Groups

- IAM = Identity and Access Management it is a global service
- Our root account is created by default.
- Users can be grouped  within the organization.
- Groups contains only users and not other groups
- One user can belong to  more than one group.
- Users or groups are assigned a JSON doc called policies
- Policies contains permissions for the user and group
- Less privilege principle - users should not be given more permission.
## IAM Policies Structure

#### IAM policies consist of:
1. **Version:** Policy language version, always include "2012-10-17"
2. **ID:** Identifier for the policy (optional)
3. **Statement:** One or more individual statements(required)
#### Statement Consists of:

1. **SID:** An identifier for the statement (Optional)
2. **Effect:** Whether the statement allow or denies access(Allow, Deny)
3. **Principal:** Account/User/Role to which this policy is applied to.
4. **Action:** List of actions this policy allows or denies.
5. **Resource:** List of resources to which the actions applied to
6. **Condition:** Condition for when this policy is in effect(optional)
Actions are applied to resources.
## How can users access AWS?
#### To access AWS there are 3 options:

1. **AWS Management console (protected by password MFA)**
2. **AWS Command Line Interface:** Protected by access keys.
3. **AWS SDK:** For code protected by access keys.
## AWS CLI
- Enables to interact with AWS services.
- Access to public APIs of AWS.
- Open Source
## AWS SDK
- Language specific APIs
- Enables access to AWS services programmatically.
- Embedded in your application.
- Supports : JS, Python, PHP, .NET, Ruby, JAVA, GO, Node, C++.
- Mobile SDKs.
- IOT Devices.
- Example: AWS CLI is built on AWS SDK for Python.
## Commands

1. This command configure AWS account.
	`aws configure`
2. To list all the users and also provides all the information about the users.
	`aws iam list -users`
3.  To check version of AWS CLI:
	`aws --version`
### What is CloudShell?
- CloudShell is cloud command line  in AWS.
## IAM Roles for Services

1. Act as a user.
2. Some services will need to perform action on your behalf
3. So to do so, we will assign permissions to AWS services with IAM roles.

## IAM Security Tools

#### IAM Credentials Report (Account level)
-  A report that lists all your accounts users and the status of their various credentials.
#### IAM Access Advisor
- Access advisor shows the service permissions given to user and when those services were last access.

## IAM Best Practices

1. Don't use root account.
2. One Physical User = One AWS account.
3. Assign the users to a group and assign permission to a group.
4. Create and use Roles for giving permission to AWS services.
