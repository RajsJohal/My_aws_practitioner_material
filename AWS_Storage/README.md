# Storage 
## Instance stores
- Instance store provides temporary block-level storage for an Amazon EC2 instance. An instance store is disk storage that is physically attached to the host computer for an EC2 instance, and therefore has the same lifespan as the instance. When the instance is terminated, you lost any data in the instance store. 

## Amazon Elastic Block Store 
- A service that provides block-level storage volumes that you can use with Amazon EC2 instances. If you stop or terminate an Amazon EC2 instance, all the data on the attached EBS volume remains available.
- To Create an EBS volume, you define the configuration (such as volume sized and type) and provision it. After you create an EBS volume, it can attach to an Amazon EC2 instance. 
- EBS volumes are used for data that needs to be persisted, it's important to back up the data. You can take incremental backups of EBS volumes by creating Amazon EBS snapshots. 

#### EBS Snapshots
- An incremental backup, this means the first backup taken of a volume copies all the data. For subsequent backups, only the blocks of data that have changed since the most recent snapshot are saved.  
- Incremental are different from full backups, in which all the data in a storage volume copies each time a backup occurs. The full backup includes data that has not changed since the most recent backup.

## Amazon Simple Storage Service (S3)
- In Objecy Storage, each object consists of data, metadata, and a key.
    - Data maybe an image, video, text or any other type of file. 
    - Metadata contains information about what the data is, how it is used, object size and so on.
    - The key is a unique identifier
- S3 stores data as objects in buckets.
- S3 Offers unlimited storage space, ,ax file size for an object in S3 is 5TB.
- Permissions can be set to control visibility and access to it. Another feature of S3 allows you to track changes to the objects over time.

#### S3 Storage Classes
- Pay for what you use
- Choose from a range of storage classe to select a fit for your business and cost needs. Consider the following factors when selecting a storage class:
    - How often you plan to retrieve your data
    - How available your data needs to be
- S3 Standard
    - Designed for frequently accessed data
    - Stores data in a minimum of three Availability Zones
    - Provides high availability for objects. Making this a good choice for a wide range of use cases, such as websites, content distribution, and data analytics. 
    - S3 Standard has a higher cost in comparison to other storage classes which are intended for infrequently accessed data and archival storage. 
- S3 Standard-Infrequent Access (S3 Standard-IA)
    - Ideal for infrequently accessed data
    - Lower storage price than S3 however has a higher retrieval price
    - Requires high availability, minimum of 4 availability zones.
- S3 One Zone-Infrequent Access (S3 One Zone-IA)
    - Stores data in a single availability zone
    - lower strage price than S3 Standard-IA
    - Save cost on storage
    - Easily reproduce data in the event of an availability zone failure
- S3 Intelligent-Tiering
    - Ideal for data with unknown or changing access patterns
    - Requires a small monthly monitoring and automation fee per object
    - The access patterns are monitored, if you haven't accessed an object for 30 consecutive days, Amazon S3 automatially moves it to the infrequent access tier, S3 Standard-IA. if you access an object in the infrequent access tier, Amazon S3 automatically moves it to the frequent access tier, S3 Standard. 
- S3 Glacier
    - Low cost storage designed for data archiving
    - Able to retrieve objects within a few minutes to hours
- S3 Glaier Deep Archive
    - Low cost object storage class ideal for archiving
    - Able to retrieve objects within 12 hours
    - When deciding between S3 Glacier and S3 Glacier Deep Dive, consider how quickly you need to retrieve archived objects. 

## Amazon Elastic File System (EFS)
#### File Storage
- In file storage, multiple clients can access data that is stored in shared file folders. In this approach, a storage server uses block storage with a local file system to organize files. Clients access data through file paths. 
- Compared to block storage and object storage, file storage is ideal for use cases in which a large number of services and resources need to access the same data at the same time. 
- EFS is scalable file system used with AWS Cloud services and on-premises resources. As you add and remove files, Amazon EFS grows and shrinks automatically. It can scale on demand to petabytes without disrupting applications. 

#### Comparison of EBS and EFS
- EBS volume stores data in a single Availability Zone.
- To attach an EC2 instance to an EBS volume, both the EC2 instance and EBS volume must reside within the same Availability Zone.
- EFS is a regional service, stores data in multiple availability zones
- Duplicate storage enables you to access data concurrently from all the availability zones in the region where a file system is located. Additionally, on-premises servers can access EFS using AWS Direct Connect.

## Amazon Relational Database Service
- Data is stored in a way that relates it to other pieces of data. 
- Relational databases use structures query language (SQL) to store and query data. This approach allows data to be stored in an easily understandable, consistent and scalable way. 
- Amazon RDS enables you to run relational databases in the AWS Cloud. 
- Amazon RDS is a managed service that automates tasks such as hardware provisioning, database setup, patching, and backups. With these capabilities you can spend less time completing administrative tasks and more time using data to innovate your applications. You can integrate Amazon RDS with other services to fulfill your business and operational needs, such as using AWS Lambda to query your database from a serverless application. 
- Amazon RDS provides a number of different security options. Many Amazon RDS database engines offer encryption at rest (protecting data while it is stored) and encryption in transit (protecting data while it is being sent and received).

#### Amazon RDS Database Engines
- Available on 6 database engines, which optimize memory, performance, or input/output (I/O). 
    - Amazon Aurora
    - PostgreSQL
    - MySQL
    - MariaDB
    - Oracle Database 
    - Microsoft SQL Server

#### Amazon Aurora 
- An enterprise-class relational database. It is compatible with MySQL and PostgreSQL relational databases. Upto 5 times faster than standard MySQL databases and upto 3 times faster than standard PostgreSQL databases. 
- Amazon Aurora helps to reduce your database costs by reducing unnecessary input/output operations, while ensuring that your database resources remain reliable and available.
- Consider Amazon Aurora if your workloads require high availability. It replicates 6 copies of your data across 3 availability zones and continuously backs up your data to Amazon S3. 

## Amazon DynamoDB
#### Nonrelational Databases
- In a nonrelational database, you create tables. A table is a place where you can store and query data. 
- Sometimes referred to as "NoSQL databases" because they use structures other than rows and columns to organize data. 
- One type of structural approach for nonrelational databases is key-value pairs. Data is organized into items (keys), and items have attributes (values). Attributes can be thought as being different features of your data. 
- In a key-value database, you can add or remove attributes from items in the table at any time. Additionally, not every item in the table has to have the same attributes.

#### DynamoDB
- A key-value database. Delivers single-digit millisecond performance at any scale. 
- Serverless, so there is no need to provision, patch or manage servers. Also there is no need to install, maintain or operate software.
- As the size of your databse shrinks or grows, DynamoDB automatically scales to adjust for changes in capacity while maintaining consistent performance, making it a suitable choice for use cases that require high performance while scaling.  

## Amazon Redshift
- Data warehousing service that you can use for big data analytics. It offers the ability to collect data from many sources and helps you understand relationships and trends across your data. 

## AWS Database Migration Service (AWS DMS)
- Enables you to migrate relational databases, nonrelational databases and other types of data stores. 
- You can move data between a source database and a target database. The source and target databases can be of the same type or different types. During the migration, your source database remains operational, reducing downtime for any applications that rely on the database. 
- For example, suppose that you have a MySQL database that is stored on premises in an EC2 instances or in Amazon RDS. Consider the MySQL databse to be your source database. Using AWS DMS, you could migrate your data to a target database, such as an Amazon Aurora database. 

#### Use Cases for AWS DMS
- Enabling developers to test applications against production data without affecting production users. 
- Combining several databases into a single database
- Sending ongoing copies of your data to other target sources instead of doing a one-time migration. 

## Additional Database Services
### Amazon DocumentDB
- A document database service that supports MongoDB workloads. 

### Amazon Neptune
- A graph database service
- Can be used to build and run applications that work with highly connected datasets, such as recommendation engines, fraud detection and knowledge graphs. 

### Amazon Quantum Ledger Database (Amazon QLDB)
- A ledger database service
- Can be used to review a complete history of all the changes that have been made to your application data.

### Amazon Managed Blockchain
- A service that you can use to create and manage blockchian networks with open-source frameworks.
- Blockchain is a distributed ledger system that lets multiple parties run transactions and share data without a central authority

### Amazon Elasticache
- A service that adds caching layers on top of your database to help improve the read times of common requests
- Supports two types of data stores: Redis and Memcached

### Amazon DynamoDB Accelerator
- In-memory cache for DynamoDB
- Helps improve response times from single-digit milliseconds to microseconds. 