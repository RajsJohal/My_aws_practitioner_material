# AWS Protection from attacks 

## Denial-of-service attacks
- A DoS attack is a deliberate attempt to make a website or application unavailable to users. 
- A good example of a DoS attack, will be flooding a website or application with excessive network traffic until the targeted website or application becomes overloaded and is no longer able to respond. If the website or application becomes unavailable, this denies service to users who are trying to make legitimate requests. 

## Distributed Denial-of-Service Attacks (DDoS)
- Multiple sources are used to start an attack that aims to make a website or application unavailable. This can come from a group of attackers or a single attacker. The single attacker can use multiple infected computers (also known as "bots") to send excessive traffic to a website or application. 
- To help minimizes the effect of DoS and DDoS attacks on your applications, you can AWS Shield.

## AWS Sheild
- A service that protects applications against DDoS attacks. AWS Shield provides two levels of protection: Standard and Advanced.

#### AWS Shield Standard
- Automatically protects all AWS customers at no cost. It protects your AWS resources from the most common, frquently occuring types of DDoS attacks.
- As network traffic comes into your applications, AWS Shield Standard uses a variety of analysis techniques to detect malicious traffic in real time and automatically mitigates it.

#### AWS Shield Advanced
- A paid service that provides detailed attack diagnostics and the ability to detect and mitigate sophisticated DDoS attacks.
- It can also be integrated with other services such as Amazon CloudFront, Amazon Route 53, and Elastic Load Balancing. Additionally, you can integrate AWS Shield with AWS WAF by writing custom rules to mitigate complex DDoS attacks. 

# Additional Security Services
## AWS Key Management Services (AWS KMS)
- Enables you to perform encryption operations through the use of cryptographic keys. 
- This service is used to create, manage and use cryptographic key. You can also control the use of keys across a wide range of services and in your applications. 
- You can select the levels of access control that you need for your keys. E.g. you can specify which IAM users and roles are able to manage keys. Alternatively, you can temprarily disable keys so that they are no longer in use by anyone. Your keys never leave AWS KMS, and you are always in control of them.  

## AWS WAF
- A web application firewall that lets you monitor network requests that come into your web applications.
- Works together with CloudFront and an Application Load Balancer. Works similar to network access controls lists, they block or allow traffic. Uses what is called a web access control list to protect AWS resources. 
- Explicitly block IP addresses. 

## Amazon Inspector
- Can perform automated security assessments
- Helps improve security and compliance of applications by running automated security assessments. Checks applications for security vulnerabilities and deviations from security best practices, such as open access to EC2 instances and installations of vulnerable software versions. 
- After the assessment, Amazon Inspector provides you with a list of security findings. The list is prioritized by severity level, including a detailed description of each security issue and a recommendation for how to fix it. 
- AWS does not guarantee that following the provided recommendations resolves every potential security issue. Under the shared responsibility model, customers are responsible for the security of their applications, processes, and tools that run on AWS services. 

## Amazon GuardDuty
- Provides intelligent threat detection for your AWS infrastructure and resources. Identifies threats by continuously monitoring the network activity and account behaviour within your AWS environment. 
- Once GuardDuty is enabled for your AWS account, GuardDuty begins monitoring your network and account activity. Continuously analyzes data from multiple AWS sources, including VPC Flow logs and DNS logs.
- If any threats are detected, detailed findings can be reviewed from the AWS Management Console. Findings include recommended steps for remediation. You can also configure AWS Lambda functions to take remediation steps automatically in response to GuardDuty's security findings. 
