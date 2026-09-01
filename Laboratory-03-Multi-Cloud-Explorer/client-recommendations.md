# Client Recommendations

## Client A – Startup Company
**Recommended Platform: Amazon Web Services (AWS)**

A startup launching a mobile application with a limited budget but expectations of rapid growth is best served by AWS. AWS provides a generous free tier, pay-as-you-go pricing, and a vast array of services that allow the team to start small and scale seamlessly as user demand increases. Its mature ecosystem and extensive documentation help a small team move quickly without needing deep specialized knowledge of every service.

**Key Services the client could use:**
- **Amazon EC2** or **AWS Lambda** for compute (serverless for cost efficiency)
- **Amazon S3** for storing user-generated content and application assets
- **Amazon RDS** or **DynamoDB** for the application database
- **Amazon API Gateway** and **Cognito** for mobile backend and user authentication

## Client B – University
**Recommended Platform: Microsoft Azure**

The university already relies on Windows Server, Microsoft 365, and Active Directory. Azure is the natural choice because it offers the deepest integration with these existing systems. Azure Hybrid Benefit can reduce licensing costs, and Microsoft Entra ID provides seamless identity federation with the on-premises Active Directory. This minimizes disruption and leverages the institution’s current Microsoft investments.

**Key Services the client could use:**
- **Azure Virtual Machines** (with Hybrid Benefit for Windows Server)
- **Microsoft Entra ID** for identity and access management
- **Azure Blob Storage** or **Azure Files** for document and research data storage
- **Microsoft 365 integration** and **Azure Active Directory Connect** for hybrid identity

## Client C – AI Research Company
**Recommended Platform: Google Cloud Platform (GCP)**

An AI/ML research company that requires high-performance computing benefits most from GCP’s leadership in artificial intelligence and machine learning. Vertex AI, access to Google’s Tensor Processing Units (TPUs), and tight integration with TensorFlow and other open-source frameworks provide a superior environment for training and deploying advanced models. BigQuery also supports large-scale data analysis that often accompanies AI research.

**Key Services the client could use:**
- **Vertex AI** for end-to-end machine learning workflows
- **Compute Engine** or **GKE** with GPU/TPU accelerators for high-performance training
- **Cloud Storage** for large datasets
- **BigQuery** for analytics on research data

## Client D – Global E-Commerce Company
**Recommended Platform: Amazon Web Services (AWS)**

A multinational e-commerce company that needs highly available infrastructure with automatic scaling is ideally matched with AWS. AWS has the most extensive global infrastructure, proven auto-scaling capabilities, and a complete set of services for building resilient, low-latency applications worldwide. Services such as CloudFront, Global Accelerator, and multi-AZ deployments help deliver consistent performance to customers around the globe.

**Key Services the client could use:**
- **Amazon EC2 Auto Scaling** and **Elastic Load Balancing** for automatic scaling and high availability
- **Amazon S3** + **CloudFront** for product images and static content delivery
- **Amazon DynamoDB** or **Aurora** for highly available, globally distributed databases
- **Amazon VPC** with multi-region architecture for resilience

## Multi-Cloud Decision Matrix (Checkpoint 6)

| **Business Requirement**     | **Recommended Platform** | **Justification** |
|------------------------------|--------------------------|-------------------|
| Startup Company              | AWS                      | Broad free tier, rapid scaling, largest ecosystem and community support for fast-moving teams |
| Enterprise Organization      | AWS or Azure             | AWS for maximum service breadth; Azure if already invested in Microsoft stack |
| Microsoft Environment        | Microsoft Azure          | Native integration with Windows, Active Directory, Microsoft 365, and Hybrid Benefit licensing |
| AI / Machine Learning        | Google Cloud Platform    | Best-in-class Vertex AI, TPUs, BigQuery, and Kubernetes support |
| Kubernetes Deployment        | Google Cloud Platform    | GKE is the most mature managed Kubernetes service (Google created Kubernetes) |
| Global Web Application       | AWS                      | Most extensive global infrastructure, CloudFront, and proven high-availability patterns |
