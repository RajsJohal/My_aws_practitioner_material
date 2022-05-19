# AWS EC2 

- Amazon Elastic Compute Cloud, provides scalable computing capacity in the AWS Cloud. Eliminates the need to invest in hardware upfront, allowing for faster develpoment and deployment of applications. Launch as many EC2 instances as you need, configure security and networking and manage storage. 

## EC2 instance Types
- General Purpose Instances
    - Provides a balance of compute, memory and networking resources. Can be used for a variety of workloads such as:
        - Application Servers
        - Gaming Servers
        - Backend servers for enterprise applications
        - Small and medium databases

- Compute Optimized Instances
    - Ideal for compute-bound applications which benefit from high-performance processors. These are ideal for workloads such as web, application, and gaming servers. 

    - Compute Optimized Instances are also used for batch processing workloads that require processing many transactions in a single group. 

- Memory Optimized Instances
    - Designed to deliver fast performance for workloads that process large datasets in memory. In computing, memory is a temporary storage area. it holds all the data and instructions that a CPU needs to be able to complete actions. Before a computer program or application is able to run, it is loaded from storage into memory. This pre loading process gives the CPU direct access to the computer program. 

    - Suppose that you have a workload that requires large amounts of data to be preloaded before running an application. This scenario maybe a high-performance database or a workload that involves performing real time processing of a large amount of unstructured data. 

- Accelerated Computing Instances
    - Utilizes hardware accelerators, or coprocessors to perform some functions more efficiently than is possible in software running on CPUs. Examples of these functions include floating-point number calculations, graphics processing and data pattern matching.  

    - In computing a hardware accelerator is a component that can expedite data processing. Accelerated computing instances are ideal for workloads such as graphics applications, game streaming and application streaming. 

- Storage Optimized Instances
    - Designed for workloads that reuire high, sequential read and write access to large data sets on local storage. Workloads that are suitable for storage optimized instances include distributed file systems, data warehousing applications and high frequency inline transaction processing (OLTP) systems.

    - IOPS, input/output operations per second is a metric that measures the performance of a storage device. It indicates how many different input or output operations a device can perform in one second. Storage optimized instances are designed to deliver tens of thousands of low-latency, random IOPS to applications. 

## EC2 Pricing
- On-Demand 
    - Ideal for short-term, irregular workloads that cannot be interrupted. No upfront costs or minimum contracts apply. The instances run continuously until you stop them, and you pay for only the compute time you use. 

    - Sample use cases for on-demand instances include developing and testing applications and running applications that have unpredictable usage patterns. On-demand instances are not recommended for workloads that last a year or longer because these workloads can experience greater cost savings using Reserved Instances.

- Amazon EC2 Savings Plans
    - AWS offers Savings Plans for several compute services, including Amazon EC2. Amazon EC2 Savings Plan enable you to reduce your compute costs by commiting to a consistent amount of compute usage for a 1 or 3 year term. 

- Reserved Instances
    - A billing discount applied to the use of On-Demand Instances in your account. You can purchase Standard Reserved and Convertible Reserved Instances for a 1 or 3 year term and Scheduled Reserved Instances for a 1 year term. At the end of the Reserved Instance term you can continue using the Amazon EC2 instance without interruption. However, you are charged On-Demand rates until you do on eof the following:
        - Terminate the instance
        - Purchase a new Reserved Instance that matches the instance attributes.

- Spot Instances
    - Ideal for workloads with flexible start and end times, or that can withstand interruptions. Spot Instances use unused Amazon EC2 computing capacity and offer you cost savings at upto 90% off On-Demand prices. 
    - Unlike Amazon EC2 Savings Plans, Spot Instances do not require contracts or a commitment to a consistent amount of compute usage. 

- Dedicated Hosts
    - Physical servers with Amazon EC2 instance capacity that is fully dedicated to your use. 
    - You can use your existing per-socket, per-core, or per-VM software licenses to help maintain license compliance. You can purchase On-Demand Hosts and Dedicated Hosts Reservations. Of all the Amazon EC2 options that were covered, Dedicated Hosts are the most expensive. 


## Scaling EC2
- Scalability involves beginning with only the resources you need and designing your architecture to automatically responf to changing demand by scaling out or in. As a result, you pay only for the resources you use. You dont have to worry about a lack of computing capacity to meet your customers needs. Amazon EC2 Auto Scaling is the AWS Service responsible for scaling processes automatically.
- Essential for making the infrastructure highly scalable.

### Amazon EC2 Auto Scaling 
- EC2 Auto Scaling enables you to automatically add or remove Amazon EC2 instances in response to changing application demand. By automatically scaling your instances in and out as needed, you are able to maintain a greater sense of application availability. 
- There are 2 approaches for auto scaling:
    - Dynamic Scaling which responds to changing demand.
    - Predictive Scaling automatically schedules the right number of Amazon EC2 instances based on predicted demand. 

###### Example of EC2 Auto Scaling
- Auto Scaling can be added to an EC2 so new instances can be added when necessary and terminate them when no longer needed. 
- You can set the number of instances you require within a certain range. You can set the following attributes of auto scaling:
    - Minimum Capacity - The number of Amazon EC2 instances that launch immediately after you have created the Auto Scaling Group.
    - Desired Capacity - You can set the desired capacity which will default to the minimum capacity if this field is not set.
    - Maximum Capacity - The auto scaling group can scale out in response to increased demand but only to a maximum number instances.

## Elastic Load Balancing
- The AWS Service that automatically distribute incoming application traffic across multiple resources, such as EC2 instances.
- The load balancer acts as the single point of contact for all incoming web traffic to your auto scaling group. As EC2 instances are added or removed in response to incoming traffic, these requests route to the load balancer first. The requests are then spread across multiple resources that will handle them such as EC2 instances, this distributes the workload across multiple instances so no single instance has to carry the bulk of the traffic.
- Elastic Load Balancers are essential for making the infrastructure highly available and scalable.

