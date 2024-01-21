+++
title = 'background'
layout = 'background'
emoji= '📝'
menu_level = ['week']
weight = 1
coursework= 'Module-cloud'
coursework_filter= 'Week 1'
+++

## Introduction to Cloud Computing

Before diving into AWS services and deployments, it's crucial to understand the fundamental concepts of cloud computing and why it has become so pivotal in today's digital landscape.

### What is Cloud Computing?

Cloud computing refers to the on-demand delivery of computing resources and services over the Internet, often referred to simply as "the cloud." These services can include things like servers, storage, databases, and networking. Instead of owning and maintaining physical data centers and servers, businesses can rent access to these resources based on their needs.

### Why is Cloud Computing Important?

Cloud computing allows organizations and individuals to avoid the complexity and cost of buying, setting up, and maintaining their own infrastructure. Here are some key advantages:

1. **Scalability**: Easily scale resources up or down based on demand.
2. **Cost-Efficiency**: Pay only for what you use, reducing upfront costs.
3. **Performance**: Benefit from the global network of secure data centers maintained by cloud providers.
4. **Speed and Agility**: Quickly deploy applications and resources.

## Exploring Servers and Virtual Machines

### What is a Server?

A server is a specialized computer designed to process requests and deliver data to another computer over the internet or a local network. While any computer can technically be configured to act as a server, most servers are dedicated, meaning they perform no other tasks than server duties.

The fundamental role of a server remains consistent, but how we deploy and manage servers has evolved with the advent of cloud computing.

#### On-Premise Servers

On-premise servers are physically located within an organization's premises. This traditional setup often requires a supporting infrastructure, including cooling systems and physical security measures. There's a high upfront capital expense due to the need for physical hardware, infrastructure, and ongoing maintenance. While it can offer optimized performance for internal users since data doesn't traverse outside the local network, it comes with the responsibility of direct maintenance and more rigid scalability. One distinct advantage is that organizations have maximum control and customization possibilities because they have direct access to the hardware.

#### Cloud Servers

In contrast, cloud servers run in a cloud computing environment and can be accessed remotely. Examples include Amazon EC2 instances or Microsoft Azure VMs. Unlike on-premise servers, cloud servers operate mainly on a pay-as-you-go model, eliminating high upfront costs. This model also offers rapid scalability; organizations can easily scale up or down based on demand without manual intervention for hardware provisioning. Maintenance is more manageable in the cloud. Providers handle most of the maintenance tasks, including software updates, security patches, and managing the physical infrastructure. The cloud model grants organizations flexibility, scalability, and potential cost savings, which is why many are transitioning to this setup.

#### Key Characteristics of Servers

High Reliability: Built to be robust and reliable in handling various tasks under different conditions.
Scalability: Capable of being expanded in size or volume to handle increased loads.
Security: Equipped with advanced security protocols to protect data and resources.

### Virtualization

Virtualization is the technology that lets you create multiple simulated environments or dedicated resources from a single, physical hardware system, making your infrastructure far more efficient and scalable.

#### Types of Virtualization

- **Server Virtualization**: Multiple operating systems can run on a single physical server as highly efficient virtual machines.

- **Network Virtualization**: A complete reproduction of a physical network, enabling a software-based network to run alongside a hardware-based network.

- **Storage Virtualization**: Pooling multiple physical storage devices into a single virtual storage device managed from a single console.

### What are Virtual Machines (VMs)?

Virtual Machines (VMs) are software emulations of physical computers. They include a virtual processor, memory, storage, and networking resources. VMs run on a physical host and are managed by a hypervisor, which controls the distribution of resources.

#### Advantages of VMs

- **Isolation**: VMs provide an isolated environment to run applications. If one VM fails or has issues, it doesn’t affect the others.

- **Resource Optimization**: VMs make efficient use of hardware, as multiple VMs can be run on a single physical server.

- **Cost-Efficiency**: VMs reduce costs related to hardware, energy, and cooling.

### Introduction to AWS EC2

Amazon Elastic Compute Cloud (Amazon EC2) is one of the most widely-used services provided by Amazon Web Services (AWS). EC2 provides scalable computing resources in the cloud, essentially offering virtual machines—known as "instances"—that can be tailored for different types of applications and workloads.

#### AWS EC2 Key Features

- **Instance Types**: EC2 provides a wide variety of instance types optimized for different use-cases, ranging from compute-optimized to storage-optimized instances. This allows you to choose the right kind of computing environment based on your application needs.

- **Elastic Load Balancing**: This feature automatically distributes incoming traffic across multiple instances for better performance and fault tolerance.

- **Security Groups**: These act as virtual firewalls that control the traffic to your instance, allowing you to specify rules based on IP protocol, port number, and source/destination IP address or CIDR block.

- **AMI (Amazon Machine Image)**: These are pre-configured templates for your instances. You can launch an instance with an AMI containing the operating system, application server, and applications required.

- **EBS (Elastic Block Store)**: Provides block storage that can be used with EC2 instances. EBS volumes can easily be resized and offer high availability and durability.

- **Elastic IPs**: These are static, public IPv4 addresses that you can allocate or release on-demand. Unlike traditional static IP addresses, Elastic IPs allow you to mask the failure of an instance or software by rapidly remapping the address to another instance in your account.

- **Auto Scaling**: This feature enables you to automatically adjust the number of EC2 instances available to your application. You can set conditions for scaling out (adding instances) or scaling in (removing instances).

- **Pricing Models**: EC2 offers various pricing options like On-Demand, Reserved Instances, and Spot Instances, allowing flexibility in managing costs.

#### AWS EC2 Benefits

- **Flexibility and Scalability**: EC2 allows you to scale your computing capacity based on the demands of your application.

- **Cost-Efficiency**: With a variety of pricing models, you can optimize costs based on your specific needs.

- **Security**: Built-in security features like Security Groups and Network ACLs provide robust protection to your instances.

- **Integration**: EC2 is well-integrated with other AWS services, making it easier to create a full-fledged application architecture in the cloud.

#### AWS EC2 Limitations

Cost Complexity: While flexible, the pricing models can be complex to understand fully and may lead to unexpected costs if not managed properly.

Resource Limits: AWS imposes certain limitations on the number of instances or type of resources you can use, although these can usually be increased upon request.

By understanding the features, benefits, and limitations of AWS EC2, you'll be better equipped to make informed decisions about how to use this service effectively for different types of cloud-based solutions.

For more information about Amazon EC2 refer to their official documentation at <https://aws.amazon.com/ec2/>

## Understanding Cloud Storage Solutions

### What is Cloud Storage?

Cloud storage is a model of storing data where the digital data is stored in logical pools, across a network of physical servers. These servers are typically owned and managed by hosting companies that provide cloud storage services.

#### Key Features of Cloud Storage

- **Accessibility**: Data can be accessed from anywhere with an internet connection.
- **Scalability**: Offers flexible storage capacity.
- **Redundancy**: Multiple backup options.
- **Security**: Data encryption and secure access controls.

### Types of Cloud Storage

- **Object Storage**: Ideal for unstructured data like photos, videos.
- **Block Storage**: Used for database storage, application storage.
- **File Storage**: For shared file systems and document storage.

### Introduction to AWS S3

Amazon Simple Storage Service (S3) is an object storage service that offers industry-leading scalability, data availability, security, and performance.

#### AWS S3 Key Features

- **Buckets**: S3 uses containers called 'buckets' to store your files.
- **Object Lifecycle Management**: Set policies to auto-transfer data to cheaper storage classes or archive them.
- **Versioning**: Keeps multiple variants of an object in the same bucket.
- **Data Transfer Acceleration**: Quickly upload files to your bucket.
- **Serverless**: Can trigger AWS Lambda functions.
- **Security**: Offers features like bucket policies and IAM to restrict access.
- **Strong Consistency**: Automatically for all objects, including overwrite PUTS and DELETES.

#### AWS S3 Benefits

- **Durability and Availability**: 99.999999999% (11 9's) durability.
- **Scalability**: Handles large data volumes.
- **Cost-Efficiency**: Pay only for the storage you use.

#### AWS S3 Limitations

- **Cost Complexity**: Pricing can be complex.
- **Permissions Complexity**: Powerful but complex permissions system.

For more information about Amazon S3 refer to their official documentation at <https://aws.amazon.com/s3/>

## Learning about Cloud Databases

### What are Cloud Databases?

Cloud databases are databases that run on a cloud computing platform, rather than on an on-premises physical server. They provide a way to store, manage, and retrieve data through a cloud service, making it accessible over the internet.

#### Key Features of Cloud Databases

- **Accessibility**: Easily accessed from anywhere through a web interface or API.
- **Scalability**: Can easily scale resources up or down based on demand.
- **Managed Service**: Includes automatic backups, updates, and maintenance.
- **Multi-Tenancy**: Allows multiple users or "tenants" to share a database instance.

### Types of Cloud Databases

- **SQL Databases**: For structured data and supports SQL querying (e.g., MySQL, PostgreSQL).
- **NoSQL Databases**: For unstructured data and supports non-SQL querying (e.g., MongoDB, DynamoDB).
- **NewSQL Databases**: Blend of SQL and NoSQL features.

### Introduction to AWS RDS

**Amazon Relational Database Service (RDS)** is a cloud-based relational database service that supports multiple types of database engines. It's part of Amazon's robust suite of cloud services.

#### Key Features

- **Managed Service**: Takes care of routine database tasks such as maintenance, backup, and patch management.
- **Scalability**: Easily resizable and supports automatic scaling.
- **Multi-AZ Deployments**: For high availability.
- **Security**: Offers features like encryption, IAM roles, and VPC to secure your databases.
- **Monitoring**: Provides in-depth monitoring through CloudWatch.

#### AWS RDS Benefits

- **Ease of Use**: Simplifies database management tasks.
- **High Availability**: Multiple availability zones for redundancy.
- **Performance**: Built-in performance metrics and tuning recommendations.

#### AWS RDS Limitations

- **Cost**: Can be expensive for large-scale deployments.
- **Limited Customization**: Not as customizable as running your own database on an EC2 instance.

Understanding AWS RDS can equip you with the knowledge to make informed choices for implementing your cloud-based database solutions.

For more information about Amazon RDS refer to their official documentation at <https://aws.amazon.com/rds/>
