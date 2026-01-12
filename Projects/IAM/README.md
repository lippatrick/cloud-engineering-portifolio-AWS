# AWS Identity and Access Management (IAM) – Practical Access Model

## Introduction
AWS Identity and Access Management (IAM) controls who can access AWS, what they can do, and under which conditions.
In real-world AWS environments, access is designed starting with two user types:

## Root User & IAM Users
Everything else (groups, policies, roles) is built on top of IAM users, not the root user.

### 1. Root User (Account Owner)
The root user is the identity created when an AWS account is first created.
It is tied to the email address used during account signup. the account is either enterprise based or personnal account. there is always one root user
per account who assigns the Level of Privilege, Unrestricted, full access meaning cannot be limited by IAM policies.

Root user can perform account-level actions that no IAM user can, change AWS account ownership, close the AWS account, modify account-wide settings
, Change billing information, enable/disable root MFA. And for that reason, this user must be used by a profeesional entrusted with the system or even almost never.

Root User Best Practices : Enable MFA immediately ||  Do not create access keys for root ||  Do not use root for daily work || Lock away root credentials securely

### 2. IAM Users (Day-to-Day Access)
An IAM user represents a person or application that needs ongoing access to AWS resources. once the setup is done by the root user, 
then they are obligated to do the rest of the activity in a new IAM user Account.  

IAM users exist to: Avoid using the root account, Apply least privilege, Enable auditing and accountability, Control access per person or service, 
Level of Privilege, No permissions by default, Permissions are explicitly assigned, Can be restricted, audited, and revoked

Types of IAM Users (Practical View)
1. Human IAM Users used by (Developers, Cloud engineers, DevOps teams, Auditors)
Access methods: AWS Management Console, AWS CLI and AWS SDKs

2. Application IAM Users (Legacy Use) used by Older applications, Third-party tools
Access method: Access Key + Secret Key. Modern AWS best practice prefers IAM Roles instead of application users.
IAM Users Created when onboarding a new team member, separating responsibilities (Dev, Ops, Audit), enforcing accountability

How IAM Users Are Created (Steps)
Log in as root or admin IAM user, Open IAM, Select Users, Click Create user, Choose (Console access, Programmatic access) ass required, Assign permissions (via groups), Enable MFA, Create user
### NOTE: remember to enable the user to autogenerate password, this provides the csv file containing the credentials to be used with ID, username and password when login.
The csv file is shared by the root user 
![image alt](https://github.com/lippatrick/cloud-engineering-portifolio-AWS/blob/main/IAM_user%20_denied.png?raw=true)

Created IAM user zac01 in my root account with denied access when logged in and password changed.

### 3. IAM Groups (Permission Management Layer)
![image alt](https://github.com/lippatrick/cloud-engineering-portifolio-AWS/blob/main/group_add.png?raw=true)

An IAM group is a way to assign permissions to multiple IAM users at once. Groups do not contain permissions directly — policies do.
Groups are centered on policies which centralize permission control, easy onboarding/offboarding, consistent access levels
Example Groups (Real-World) Administrators || Developers || DevOps || ReadOnly-Auditors

### 4. IAM Policies (Permission Definition)
What is an IAM Policy?
A policy defines what actions are allowed or denied on specific AWS resources. Policies do not grant access on their own — they must be attached to: Groups, Users, Roles, Policy Privilege Control, Fine-grained and many more.

Policies are JSON format files.

![image alt](https://github.com/lippatrick/cloud-engineering-portifolio-AWS/blob/main/Policy.png?raw=true)
default AmazonFullAccess Policy S3 bucket demo (JSON code)

## Conclusion
A secure AWS environment starts with locking down the root user, creating IAM users for humans, managing access through groups and policies, and using roles for services and automation.
This design reflects real-world AWS security architecture used in enterprise and production environments.



