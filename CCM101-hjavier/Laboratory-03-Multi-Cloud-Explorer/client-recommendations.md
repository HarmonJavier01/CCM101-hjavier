# Client Recommendations & Multi-Cloud Decision Matrix

## Multi-Cloud Decision Matrix (Checkpoint 6)

| Business Requirement | Recommended Platform | Justification |
| :--- | :--- | :--- |
| **Startup Company** | AWS | Comprehensive free tier, serverless options, and elastic scalability that matches early-stage growth. |
| **Enterprise Organization** | Microsoft Azure / AWS | High compliance standards, enterprise SLAs, and strong governance frameworks. |
| **Microsoft Environment** | Microsoft Azure | Direct compatibility with Active Directory, Windows Server, and Microsoft 365 licensing. |
| **AI / Machine Learning** | Google Cloud Platform | Optimized TPU hardware, Google-engineered ML libraries, and managed Vertex AI workflows. |
| **Kubernetes Deployment** | Google Cloud Platform | Google created Kubernetes, and GKE remains the most reliable and advanced managed Kubernetes service. |
| **Global Web Application** | AWS | Largest edge network with CloudFront and multi-region deployment redundancy. |

---

## Scenario Analyses (Checkpoint 4)

### Client A – Startup Company
* **Recommended Platform**: Amazon Web Services (AWS)
* **Explanation**: AWS is best suited for startups due to the AWS Free Tier, flexible pay-as-you-go pricing, and rapid scalability. Its managed services allow lean development teams to launch mobile backends without managing underlying hardware. As the application grows, AWS supports automated scaling without needing architectural rewrites.
* **Recommended Services**: AWS Amplify, Amazon EC2, Amazon DynamoDB.

### Client B – University
* **Recommended Platform**: Microsoft Azure
* **Explanation**: Because the university already relies heavily on Windows Server, Microsoft 365, and Active Directory, Azure provides native synchronization through Microsoft Entra ID. This avoids the overhead of managing separate credential systems and saves software costs via the Azure Hybrid Benefit. Migration of legacy infrastructure remains smooth and secure.
* **Recommended Services**: Microsoft Entra ID, Azure Virtual Machines, Azure SQL Database.

### Client C – AI Research Company
* **Recommended Platform**: Google Cloud Platform (GCP)
* **Explanation**: GCP specializes in cutting-edge compute infrastructure for Machine Learning and AI research. It provides native access to custom Tensor Processing Units (TPUs) and an integrated Vertex AI platform that speeds up deep learning model training. Its high-throughput data processing handles research workloads efficiently.
* **Recommended Services**: Vertex AI, Compute Engine (with GPU/TPU acceleration), Google Cloud Storage.

### Client D – Global E-Commerce Company
* **Recommended Platform**: Amazon Web Services (AWS)
* **Explanation**: AWS provides the global footprint, high availability, and auto-scaling capabilities needed for large-scale international e-commerce. Services like CloudFront and multi-AZ deployments ensure fast page loads and zero downtime during peak seasonal traffic spikes. The managed database offerings provide reliable transaction processing worldwide.
* **Recommended Services**: Amazon CloudFront, Elastic Load Balancing (ELB), Amazon Aurora.