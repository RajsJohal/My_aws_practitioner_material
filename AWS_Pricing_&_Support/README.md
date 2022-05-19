# AWS Pricing and Support

## AWS Free Tier
- Enables you to begin using certain services without having to worry about incurring costs for the specified period.
- 3 types:
    - Always Free, e.g. AWS Lambda
    - 12 months free, e.g. Specific amounts of S3 Standard, thresholds for monthly hours of EC2 compute time, and amounts of Amazon CloudFront data trasfer out.
    - Trials, e.g. Amazon Inspector offers a 90-day free trial. Amazon Lighsail offers 750 free hours of usage over a 30-day period.

## AWS Pricing Concepts
- AWS offers a range of cloud computing services with pay-as-you-go pricing. 
- Pay for what you use = Pay exactly for the amount of resources that you actually use without requiring long-term contracts or complex licensing. 
- Pay less when you reserve = Some services offer reservation options that provide a significant discount compared to On-demand instance pricing. 
- Pay less with volume-based discounts when you use more = Some service offer tiered pricing, so the per-unit cost is incrementally lower with increased usage. 

## AWS Pricing Calculator
- Lets you explore AWS services and create an estimate for the cost of your use cases on AWS. You can organize your AWS estimates by groups that you define. A group can reflect how your company is organized, such as providing estimates by cost centre. 
- An estimate can be saved and shared with others. 
- AWS Pricing Calculator allows you to enter details such as the kind of OS you need, memory requirements, I/O requirements. You can also review an estimated comparison of different EC2 instance types across AWS regions. 

## AWS Billing and Cost Management Dashboard
- Monitor usage, analyze and control your costs and pay your AWS bill.
- Compare current month-to-date balance with previous month and get a forecast of the next month based on current usage.
- View month-to-date spend by service.
- View Free Tier usge by service
- Access cost explorer and creat budgets
- Purchase and manage Savings Plans 
- Publish AWS Cost and Usage Reports

## Consolidated Billing
- A feature of AWS Organizations enables you to receive a single bill for all AWS accounts in your organization. Easily track the combined costs of all the linked accounts in your organization.
- Default max number of accounts allowed for an organization is 4 but can be increased if you contact AWS Support. 
- On your monthly bill, you can review itemized changes incurred by each account. 
- Consolidated billing grants the ability to share bulk discount pricing, Savings Plans, and Reserved Instances across accounts in your organization. For example, is one account does not have enough monthly usage to qualify for discount pricing. However, when multiple accounts are combined, their aggregated usage may result in a benefit that applies across all accounts in the organization. 

## AWS Budgets
- Create budgets to plan service usgae, service costs and instance reservations. 
- Information in AWS Budgets updates three times a day.
- Custom alerts can be set in case usage exceeds the budgeted amount.
- Can also view forecasted usage against your budget to determie how to adjust your usage. 

## AWS Cost Explorer
- A tool used to visualize, understand and manage your AWS costs and usage over time. 
- Includes a default report of the costs and usage for your top five cost-accuring AWS services. You can apply custom filters and group to analyze your data. 

## AWS Support
- AWS offers 4 different support plans to help troubleshoot issues, lower costs and efficiently use AWS services. 
    - Basic
    - Developer
    - Business
    - Enterprise

#### Basuc Support
- Free for all AWS customers. Includes access to whitepapers, documentation, and support communities. You can also contact AWS for billing questions and service limit increases. 
- Access to a limited selection of AWS Trusted Advisor checks. Additionally, you can use the AWS Personal Health Dashboard, a tool that provides alerts and remediation guidance when AWS is experiencing events that may affect you. 

#### Developer, Business and Enterprise Support
- All these plans include all the benefits of Basic Support, in addition to the ability to open an unrestricted number of technical support cases. These three support plans have pay-by-the-month pricing and require no long-term contracts. 
- The developer plan is the cheapest of the three, then business and then enterprise. 
- Developer Support:
    - Best practice guidance
    - Client-side diagnostic tools
    - Building-block architecture support, which consists of guidance for how to use AWS offerings, features and services together. 
- Business Support:
    - Use-case guidance to identify AWS offerings, features, and services that can best support your specific needs. 
    - All AWS Trusted Advisor checks
    - Limited support for 3rd party software, such as common OS and application stack components
- Enterprise Support:
    - Application architecture guidance, which is a consultative relationship to support your company's specific use cases and applications.
    - Infrastructure event management: A short-term engagement with AWS Support that helps your company gain a better understanding of your use cases. This also provides your company with a architectural and scaling guidance. 
    - A Technical Account Manager.

#### Technical Account Manager (TAM)
- Primary point of contact at AWS. 
    - They provide guidance, architectural reviews, and ongoing communication with your company as you plan, deploy, and optimize your applications. 
    - Offer expertise across the full range of AWS services. Assist with design solutions that efficiently use mutliple services together through an integrated approach. 