# Security

## Shared Responsible Model
- The resources that are utilised in AWS need to be monitored and secured, this is the reponsibility of both AWS and the user. 
- The AWS environment should not be treated as a single object, rather you treat the environment as a collection of parts that build upon each other. AWS is responsible for some parts of your environment and the customer is responsible for the other parts. 
- The shared responsibility model divides into customer responsibilities (referred to as security in the cloud) and AWS repsonsibilities (referred to as the security of the cloud)

#### Customers: Security in the cloud
- Customers are responsible of everything that they create and put in the AWS cloud. 
- When using AWS, the customer maintains complete control over your content. you are responsible for managing security requirements for your content, including which content you chose to store on AWS, which AWS services you use, and who has access to that content. you also control how access rights are granted, managed and revoked. 
- Steps taken to deploy security include:
    - Selecting, configuring and pathcing the operating systems that will run on EC2 instances, configuring security groups, and managing user accounts. 

#### AWS: Security of the cloud
- AWS operates, manages and controls the components at all layers of infrastructure. This includes areas such as the host OS, vitualization layer and even the physical security of the data centres from which services operate. 
- AWS is repsonsible for protecting the global infrastructure that runs all of the services offered in the AWS Cloud. This infrastructure includes AWS Regions, Availability Zones, and edge locations. 
- AWS manages the security of the cloud, specifically the physical infrastructure that hosts your resources, which include:
    - Physical Security of data centres
    - Hardware and Software infrastructure
    - Network infrastructure
    - Virtualization infrastructure
- AWS provides reports from third-party auditors. These auditors have verified its compliance with a variety of computer security and regulations. 

# User Permissions and Access
## AWS Identity and Access Management (IAM)
- Enables you to manage access to AWS services and resources securely. 
- Provides flexibility to configure access based on your company's specific operational and security needs. This is achieved by using a combination of IAM features, which are explored in detail in this lesson:
    - IAM Users, Groups and Roles
    - IAM Policies
    - Multi-Factor Authentication

## AWS Account Root User
- When you first create an AWS account, you begin with an identity known as the root user.
- Root user is accessed by signing in with the email address and password that you used to create your AWS account.

## IAM Users
- An IAM user is an identity that you create in AWS. It represents the person or application that interacts with AWS services and resources. It consists of a name and credentials. 
- By default, when you create a new IAM user in AWS, it has no permissions associated with it. To allow the IAM user to perform specific actions in AWS, such as launching an Amazon EC2 instance or creating an Amazon S3 bucket, you must grant the IAM user the necessary permissions. 

## IAM Policies
- A document that allows or denies permissions to AWS services and resources.
- IAM policies enable you to customize users levels of access to resources. For example, you can allow users to access all of the S3 buckets within your AWS account, or only a specific bucket. 
- IAM Policies allow specific actions for specific resources, this policy can be attached to a specific resource-id and a specific IAM user.

## IAM Groups
- IAM Group is a collection of IAM Users. 
- You can assign a IAM policy to a group and all users within the group have all the permissions specified in the policy.

## IAM Roles
- It is an identity that you can assume to gain temporary access to permissions. 
- Before an IAM user, application, or service can assume an IAM role, they must be granted permissions to switch to the role. When someone assume an IAM role, they abandon all previous permissions that hey had under a previous role and assume the permissions of the new role. 

## Multi-factor Authentication
- Provides an extra layer of security for your AWS account. 
