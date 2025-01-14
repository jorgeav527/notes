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