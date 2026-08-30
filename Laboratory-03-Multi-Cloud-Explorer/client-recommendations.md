# Client Recommendations

## Client A – Startup Company
**Scenario:** The client is a startup with a limited budget and expects rapid growth.
### Recommended Platform: AWS

AWS is a suitable choice for the startup because it provides a wide range of cloud services that can support a new mobile application. The company can begin with the resources it needs and increase its infrastructure as the number of users grows. AWS also provides managed services that can reduce the amount of infrastructure the startup needs to maintain.

### Recommended Services
Amazon EC2 can be used for application computing.
Amazon S3 can be used for object and file storage.
Amazon RDS can be used for a relational database.
Amazon DynamoDB can also be considered for applications requiring a NoSQL database.

## Client B – University
**Scenario:** The university already uses Windows Server, Microsoft 365, and Active Directory. These requirements are explicitly given in the activity.

### Recommended Platform: Microsoft Azure
Microsoft Azure is the most appropriate platform for the university because it already uses Windows Server, Microsoft 365, and Active Directory. Azure provides strong integration with Microsoft's existing technologies and can help the university migrate selected services to the cloud. Azure can also support hybrid environments where some resources remain on-premises while others operate in the cloud.

### Recommended Services
Azure Virtual Machines can host Windows Server workloads.
Microsoft Entra ID can support identity and access management.
Azure SQL Database can provide managed relational database capabilities.
Azure Blob Storage can provide cloud object storage.

## Client C – AI Research Company
**Scenario:** The activity states that Client C is an AI research company requiring high-performance computing.

### Recommended Platform: Google Cloud Platform
Google Cloud is an appropriate choice for the AI research company because it provides strong Artificial Intelligence and Machine Learning capabilities. The company can use cloud computing resources for demanding workloads and use managed AI services to develop and test machine learning applications. Google Cloud also provides Kubernetes capabilities for organizations that want to deploy containerized applications.

### Recommended Services
Compute Engine can provide virtual machines for computing workloads.
Vertex AI can support artificial intelligence and machine learning development.
Google Kubernetes Engine can support Kubernetes-based applications.
Cloud Storage can store datasets and other research files.

## Client D – Global E-Commerce Company
**Scenario:** The activity says this company serves customers around the world and requires highly available infrastructure with automatic scaling.

### Recommended Platform: AWS
AWS is a strong choice for a global e-commerce company because it provides a large global infrastructure and services designed for scalable applications. The company can deploy its application across multiple locations and use automatic scaling to handle changes in customer demand. AWS also provides services for content delivery, load balancing, storage, databases, and application computing.

### Recommended Services
Amazon EC2 can provide application computing resources.
Elastic Load Balancing can distribute application traffic.
Amazon S3 can provide object storage.
Amazon RDS can provide a managed relational database.
Amazon CloudFront can provide content delivery for users in different locations.

# Multi-Cloud Decision Matrix

| Business Requirement    | Recommended Platform | Justification                                       |
| ----------------------- | -------------------- | --------------------------------------------------- |
| Startup Company         | AWS                  | Broad service selection and scalable infrastructure |
| Enterprise Organization | AWS                  | Wide range of services and global infrastructure    |
| Microsoft Environment   | Azure                | Strong integration with Microsoft technologies      |
| AI / Machine Learning   | GCP                  | Strong AI and machine learning capabilities         |
| Kubernetes Deployment   | GCP                  | Strong Kubernetes capabilities through GKE          |
| Global Web Application  | AWS                  | Global infrastructure and scalable services         |
