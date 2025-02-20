# 🏠 MOC

## What is a client-server model?
In computing, a **client** can be a web browser or desktop application that a person interacts with to make requests to computer servers. A **server** can be services, such as Amazon Elastic Compute Cloud (Amazon EC2) – a type of virtual server. 
	
About deployment models.

| **Deployment Model**       | **Description**                                                                                                                                       | **Example Use Case**                                                                                            |
| -------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| **Cloud-Based Deployment** | - Run, migrate, or build applications in the cloud.<br>- Use low-level infrastructure or higher-level services to reduce management overhead.         | An application built with virtual servers, databases, and networking components, fully based in the cloud.      |
| **On-Premises Deployment** | - Resources are deployed in on-premises data centers.<br>- Uses virtualization and resource management tools.<br>- Known as private cloud deployment. | Applications running on technology fully kept in an on-premises data center with enhanced resource utilization. |
| **Hybrid Deployment**      | - Combines cloud-based and on-premises resources.<br>- Suitable for legacy applications or regulatory requirements.<br>- Enables cloud integration.   | Legacy applications remain on premises, while batch data processing and analytics services run in the cloud.    |
## EC2
- Amazon Elastic Compute Cloud (EC2) provides secure and resizable compute capacity in the cloud.
- It enables running applications on virtual servers (EC2 instances) in the AWS Cloud.
- **Multitenancy**: Instances share physical hardware securely using a hypervisor.
- **Configuration Control**: Customize the operating system (Windows or Linux), software, and networking settings.
- **Resizable Instances**: Adjust instance size based on resource needs.
- **Networking Control**: Define public or private access to instances.
- EC2 instances are isolated from each other, ensuring secure multitenant environments.
- The compute as a Service Model, provides high availability of compute capacity manage by AWS.

### Types of EC2 instances
- **General purpose instances**: provide a balance of compute, memory, and networking resources.
	- application servers
	- gaming servers
	- backend servers for enterprise applications
	- small and medium databases
- **Compute optimized instances**: compute-bound applications that benefit from high-performance processors.
	- compute-intensive applications servers
	- dedicated gaming servers
	- batch processing workloads that require processing many transactions in a single group
- **Memory optimized instances**: are designed to deliver fast performance for workloads that process large datasets in memory.
	- high-performance database
	-  real-time processing of a large amount of unstructured data
- **Accelerated computing instances**: use hardware accelerators, or coprocessors, to perform some functions more efficiently than is possible in software running on CPUs.
	- functions include floating-point number calculations
	- graphics applications processing, and data pattern matching.
	- game streaming
- **Storage optimized instances**: are designed for workloads that require high, sequential read and write access to large datasets on local storage. *Storage optimized instances are designed to deliver tens of thousands of low-latency, random IOPS->It indicates how many different input or output operations a device can perform in one second. to applications.*
	- distributed file systems
	- data warehousing applications
	- high-frequency online transaction processing (OLTP) systems
### EC2 pricing
- **On-Demand Instances** are ideal for short-term, irregular workloads that cannot be interrupted.
- **Reserved Instances** are a billing discount applied to the use of On-Demand Instances in your account. There are two available types of Reserved Instances:
	- Standard Reserved Instances: This option is a good fit if you know the EC2 instance type and size you need for your steady-state applications and in which AWS Region you plan to run them.
	- Convertible Reserved Instances:  If you need to run your EC2 instances in different Availability Zones or different instance types, then Convertible Reserved Instances might be right for you.
- **EC2 Instance Savings Plans** reduce your EC2 instance costs when you make an hourly spend commitment to an instance family and Region for a 1-year or 3-year term. This term commitment results in savings of up to 72 percent compared to On-Demand rates.
- **Spot Instances** are ideal for workloads with flexible start and end times, or that can withstand interruptions. Spot Instances use unused Amazon EC2 computing capacity and offer you cost savings at up to 90% off of On-Demand prices.
- **Dedicated Hosts** are physical servers with Amazon EC2 instance capacity that is fully dedicated to your use. Dedicated Hosts are the most expensive.