# Additional Compute Services

## Severless Computing
- Code that is run on servers. but you do not need to provision or manage these servers. Serverless computing allows you to focus on innovating new products and features instead of maintaining servers. 
- Another benefit of serverless computing is the flexibility to scale serverless applications automatically. Serverless computing can adjust the applications capacity by modifying the units of consumptions such as throughput and memory. 
- AWS Service for serverless computing is AWS Lambda.

## AWS Lambda
- AWS Service which allows you to run code without the need to provision or manage servers. 
- Pay only for the compute time that you consume. Charges apply only when your code is running. 

#### How AWS Lambda works
- Upload code to Lambda
- Set your code to trigger from an event source, such as AWS services, mobile pplications or HTTP endpoints
- Lambda runs your code only when triggered
- Pay only for the compute time that you use. 

## Containerized Applications
#### Containers
- Provide a standard way to package your application's code and dependencies into a single object. You can also use containers for processes and workflows in which there are essential requirements for security, reliabaility and scalability. 

#### Amazon Elastic Container Service (ECS)
- Highly scalable, high-performance container management system that enables you to run and scale containerized applications on AWS. 

#### Amazon Elastic Kubernetes Service (EKS)
- A fully managed service that you can use to run Kubernetes on AWS.
- Kubernetes is an open-source software that enables you to deploy and manage containerized applications at scale. A large community of volunteers maintains Kubernetes, and AWS actively works together with the Kubernetes community. As new features and functionalities release for Kubernetes applications, you can easily apply these to your applications managed by Amazon EKS.

#### AWS Fargate
- A serverless compute engine for containers. It works with both ECS and EKS. 
- Manages server infrastructure for you. Focus more on innovating and developing your applications, and you pay only for the resource that are required to run your containers. 