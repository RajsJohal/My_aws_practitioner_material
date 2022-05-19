# AWS Monitoring

## Amazon CloudWatch
- A web service that enables you to monitor and manage various metrics and configure alarm actions based on data from those metrics. 
- CloudWatch uses metrics to represent the data points for your resources. AWS services send metrics to CloudWatch then uses these metrics to create graphs automatically that show how performance has changed over time. 

#### CloudWatch Alarms
- You can create alarms that automatically perform actions if the value of your metric has gone above or below a predefined threshold. 
- For example, you can create a CloudWatch alarm that will automatically stop an EC2 when CPU Utilization percentage has remained below a certain threshold for a specified period. When configuring the alarm, you can also specify a notification whenever the alarm is triggered. 

#### CloudWatch Dashboard
- This feature enables you to access all the metrics for your resources from a single location. For example, you can use a CloudWatch dashboard to monitor the CPU utilization of an EC2 instance, number of requests made to an Amazon S3 bucket, and more. You can also customize dashboards for different business purposes, applications or resources. 

## AWS CloudTrail
- Records API calls for your account. 
- The recorded information includes the identity of the API caller, the time of the API call, the source IP adress of the API caller, and more.
- It is essentially a log of actions some has left behind.
- View a complete history of user activity and API calls for your applications and resources. 

#### CloudTrail Insights
- Optional feature within allows CloudTrail to automatically detect unusual API activities in your AWS account. 

## AWS Trusted Advisor
- A web service that inspects your AWS environment and provides real-time recommendations in accordance with AWS best practices.
- Trusted Advisor compares its findings to AWS best practices in 5 categories:
    - Cost
    - Optimization
    - Performance
    - Security
    - Fault Tolerance
    - Service Limits
- For checks in each category, Trusted Advisor offers a list of recommended actions and additional resources to learn more about AWS best practices. 

#### AWS Trusted Advisor Dashboard
- View completed checks for cost optimization, performance, security, fault tolerance, and service limits. 
- For each category:
    - Green Check indicates the number of items for which it detected no problems
    - Orange triangle represents the number of recommended investigations
    - Red Circle represents number of recommended actions.