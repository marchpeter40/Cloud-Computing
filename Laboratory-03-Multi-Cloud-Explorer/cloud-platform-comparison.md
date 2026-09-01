# Cloud Platform Comparison

## Comparison Table

| **Category**              | **AWS**                          | **Microsoft Azure**                     | **Google Cloud Platform**              |
|---------------------------|----------------------------------|-----------------------------------------|----------------------------------------|
| Launch Year               | 2006                             | 2010                                    | 2008                                   |
| Compute Service           | Amazon EC2                       | Azure Virtual Machines                  | Compute Engine                         |
| Storage Service           | Amazon S3                        | Azure Blob Storage                      | Cloud Storage                          |
| Networking Service        | Amazon VPC                       | Azure Virtual Network (VNet)            | Virtual Private Cloud (VPC)            |
| Identity Service          | AWS IAM                          | Microsoft Entra ID (Azure AD)           | Cloud Identity / IAM                   |
| Primary Strength          | Broadest service catalog & maturity | Microsoft ecosystem integration & hybrid | AI/ML, data analytics & Kubernetes     |
| Ideal Organizations       | Startups to large enterprises needing maximum flexibility | Organizations already invested in Microsoft technologies | Data-driven, AI-focused, and container-native companies |

## Discussion Questions

### 1. Which cloud provider offers the broadest range of services?
AWS offers the broadest range of services with over 200 fully featured offerings covering nearly every imaginable use case. Its long head start since 2006 has allowed continuous expansion into specialized domains such as IoT, quantum computing, and industry-specific solutions. This breadth makes AWS a safe default choice when requirements are diverse or not yet fully defined.

### 2. Which provider best integrates with Microsoft technologies?
Microsoft Azure provides the best integration with Microsoft technologies. It offers native support for Windows Server, Active Directory (via Entra ID), Microsoft 365, SQL Server, and .NET applications. Features such as Azure Hybrid Benefit allow organizations to reuse existing Microsoft licenses, significantly reducing costs when migrating or extending on-premises Microsoft environments to the cloud.

### 3. Which provider is strongest in Artificial Intelligence and Kubernetes?
Google Cloud Platform is strongest in Artificial Intelligence and Kubernetes. GCP provides industry-leading tools such as Vertex AI, access to custom TPUs, and BigQuery for analytics. Google originally developed Kubernetes, and Google Kubernetes Engine (GKE) is widely considered the most mature and feature-rich managed Kubernetes service, including Autopilot mode for simplified operations.

### 4. Which cloud platform would you personally choose and why?
Personally, I would choose AWS for most general-purpose projects because of its unmatched service breadth, mature ecosystem, extensive documentation, and largest community support. The wide availability of learning resources and third-party tools reduces risk and accelerates development. For specialized AI/ML or heavy Kubernetes workloads I would evaluate GCP, and for pure Microsoft environments I would select Azure.

## Equivalent Services Reference Table (Checkpoint 5)

| **Service Category**   | **AWS**              | **Azure**                  | **GCP**                  |
|------------------------|----------------------|----------------------------|--------------------------|
| Virtual Machine        | Amazon EC2           | Azure Virtual Machines     | Compute Engine           |
| Object Storage         | Amazon S3            | Azure Blob Storage         | Cloud Storage            |
| Identity Management    | AWS IAM              | Microsoft Entra ID         | Cloud Identity / IAM     |
| SQL Database           | Amazon RDS / Aurora  | Azure SQL Database         | Cloud SQL                |
| Kubernetes             | Amazon EKS           | Azure Kubernetes Service (AKS) | Google Kubernetes Engine (GKE) |
