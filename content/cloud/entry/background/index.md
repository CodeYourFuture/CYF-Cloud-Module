+++
title = 'background'
layout = 'background'
emoji= '📝'
menu_level = ['week']
weight = 1
coursework= 'Module-cloud'
coursework_filter= 'Week 1'
+++

Before diving into AWS services and deployments, it's crucial to understand the fundamental concepts of cloud computing and why it has become so pivotal in today's digital landscape.

## What is Cloud Computing?

Cloud computing refers to the on-demand delivery of computing resources and services over the Internet, often referred to simply as "the cloud." These services can include things like servers, storage, databases, and networking. Instead of owning and maintaining physical data centers and servers, businesses can rent access to these resources based on their needs.

## Why is Cloud Computing Important?

Cloud computing allows organizations and individuals to avoid the complexity and cost of buying, setting up, and maintaining their own infrastructure. Here are some key advantages:

1. **Scalability**: Easily scale resources up or down based on demand.
2. **Cost-Efficiency**: Pay only for what you use, reducing upfront costs.
3. **Performance**: Benefit from the global network of secure data centers maintained by cloud providers.
4. **Speed and Agility**: Quickly deploy applications and resources.

<iframe width="800" height="315" style="border: 1px solid #843dff; padding: 10px; margin-bottom: 40px" src="https://www.youtube.com/embed/M988_fsOSWo?si=Si8SsJWLUJdxKWoN" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## What is a Server?

A server is a specialized computer designed to process requests and deliver data to another computer over the internet or a local network. While any computer can technically be configured to act as a server, most servers are dedicated, meaning they perform no other tasks than server duties.

The fundamental role of a server remains consistent, but how we deploy and manage servers has evolved with the advent of cloud computing.

### On-Premise Servers

On-premise servers are physically located within an organization's premises. This traditional setup often requires a supporting infrastructure, including cooling systems and physical security measures. There's a high upfront capital expense due to the need for physical hardware, infrastructure, and ongoing maintenance. While it can offer optimized performance for internal users since data doesn't traverse outside the local network, it comes with the responsibility of direct maintenance and more rigid scalability. One distinct advantage is that organizations have maximum control and customization possibilities because they have direct access to the hardware.

### Cloud Servers

In contrast, cloud servers run in a cloud computing environment and can be accessed remotely. Examples include Amazon EC2 instances or Microsoft Azure VMs. Unlike on-premise servers, cloud servers operate mainly on a pay-as-you-go model, eliminating high upfront costs. This model also offers rapid scalability; organizations can easily scale up or down based on demand without manual intervention for hardware provisioning. Maintenance is more manageable in the cloud. Providers handle most of the maintenance tasks, including software updates, security patches, and managing the physical infrastructure. The cloud model grants organizations flexibility, scalability, and potential cost savings, which is why many are transitioning to this setup.

## Virtualization

Virtualization is the technology that lets you create multiple simulated environments or dedicated resources from a single, physical hardware system, making your infrastructure far more efficient and scalable.

- **Server Virtualization**: Multiple operating systems can run on a single physical server as highly efficient virtual machines.
- **Network Virtualization**: A complete reproduction of a physical network, enabling a software-based network to run alongside a hardware-based network.
- **Storage Virtualization**: Pooling multiple physical storage devices into a single virtual storage device managed from a single console.

<iframe width="800" height="315" style="border: 1px solid #843dff; padding: 10px; margin-bottom: 40px" src="https://www.youtube.com/embed/UBVVq-xz5i0?si=LjVg4wPxcG_Un9Iy" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## What are Virtual Machines (VMs)?

Virtual Machines (VMs) are software emulations of physical computers. They include a virtual processor, memory, storage, and networking resources. VMs run on a physical host and are managed by a hypervisor, which controls the distribution of resources.

### Advantages of VMs

- **Isolation**: VMs provide an isolated environment to run applications. If one VM fails or has issues, it doesn’t affect the others.
- **Resource Optimization**: VMs make efficient use of hardware, as multiple VMs can be run on a single physical server.
- **Cost-Efficiency**: VMs reduce costs related to hardware, energy, and cooling.

## This weeks projects...

This week, you'll be working with three key tools - EC2, S3 and RDS. You'll be using them to deploy your CYF Hotel project to the cloud.

### AWS EC2

Amazon Elastic Compute Cloud (Amazon EC2) is one of the most widely-used services provided by Amazon Web Services (AWS). EC2 provides scalable computing resources in the cloud, essentially offering virtual machines - known as "instances" - that can be tailored for different types of applications and workloads.

You can learn move about EC2 at the official documentation at <https://aws.amazon.com/ec2/>

Learn more about what an EC2 is and how to set one up here

<iframe width="800" height="315" style="border: 1px solid #843dff; padding: 10px; margin-bottom: 40px" src="https://www.youtube.com/embed/eaicwmnSdCs?si=xkfAv5L8H21E50-_" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

### AWS S3

Amazon Simple Storage Service (S3) is an object storage service that offers industry-leading scalability, data availability, security, and performance.

For more information about Amazon S3 refer to their official documentation at <https://aws.amazon.com/s3/>

<iframe width="800" height="315" style="border: 1px solid #843dff; padding: 10px; margin-bottom: 40px" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

### AWS RDS

Cloud databases are databases that run on a cloud computing platform, rather than on an on-premises physical server. They provide a way to store, manage, and retrieve data through a cloud service, making it accessible over the internet.

**Amazon Relational Database Service (RDS)** is a cloud-based relational database service that supports multiple types of database engines. It's part of Amazon's robust suite of cloud services.

For more information about Amazon RDS refer to their official documentation at <https://aws.amazon.com/rds/>

<iframe width="800" height="315" style="border: 1px solid #843dff; padding: 10px; margin-bottom: 40px" src="https://www.youtube.com/embed/tLp8pPNdDXQ?si=ibuibsiGzPJkgseY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
