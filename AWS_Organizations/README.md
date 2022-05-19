# AWS Organizations
- For a company that has multiple AWS accounts. You can use AWS Organizations to consolidate and manage multiple AWS accounts within a central location. 
- When you create an organization, AWS Organizations automatically creates a root, which is the parent container for all the accounts in your organization. 
- In AWS Organizations, you can centrally control permissions for the accounts in your organization by using service control policies (SCPs). SCPs enable you to place restrictions on the AWS services, resources and indiviual API actions that users and toles in each account can access. 

## Organizational Units
- In AWS Organizations, you can group accounts into organizational units (OUs) to make it easier to manage accounts with similar business or security requirements. When you apply a policy to an OU, all the accounts in the OU automatically inherit permissions specified in the policy. 
- By organizing seperate accounts into OUs, you can more easily isolate workloads or applications that have specific security requirements. For instance, if your company has accounts that can access only the AWS services that meet certain regulatory requirements, you can put these accounts into one OU. Then, you can attach a policy to the OU that blocks access to all other AWS services that do not meet the regulatory requirements. 

## AWS Artifact 
- Depending on your company's industry, you may need to uphold specific standards. An audit or inspection will ensure that the company has met those standards. 
- AWS Artifact is a service that provides on-demand access to AWS security and compliance reports and select online agreements. AWS Artifact consists of two main sections: AWS Artifact Agreement and AWS Artifact Reports. 

#### AWS Artifact Agreements
- You can review, accept and manage agreements for an individual account and for all your accounts in AWS Organizations. Different types of agreement are offered to address the needs of customers who are subject to specific regulations. 

#### AWS Artifact Reports
- Suppose that a member of your company's development team is building an application and needs more information about their responsibility for complying with certain regulatory standards. You can advise them to access this information in AWS Artifact Reports. 
- AWS Artifact Reports provide compliance reports from third-party auditors. These auditors have tested and verified that AWS is compliant with a variety of global, regional, and industry-specific security standards and regulations. AWS Artifact Reports remains up to date with the latest reports released. You can provide the AWS audit artifacts to your auditors or regulators as evidence of AWS security controls. 

## Customer Compliance Centre
- Contains resources to help you learn more about AWS compliance. 
- In the customer compliance centre, you can read customer compliance stories to discover how companies in regulated industries have solved various compliance, governance and audit challenges. 
- You can access compliance whitepapers and documentation on topics such as:
    - AWS answers to key compliance questions
    - An overview of AWS risk and compliance
    - An auditing security checklist
- Additionally, the customer compliance centre includes an auditor learning path. This learning path is designed for individuals in auditing, compliance, and legal roles who want to learn more about how thier internal operations can demonstrate compliance using the AWS Cloud. 