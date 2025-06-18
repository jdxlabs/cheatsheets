# Cloud equivalents

## Platforms specificities
| Description | AWS | GCP | Azure | Scaleway | OVHCloud |
| ----------- | ------- | --- | ----- | -------- | --------- |
| Nb of services | 200+ | 200+ | 100+ | 50+ | 80+ |
| Compute / VMs | Elastic Cloud Compute (EC2) | Google Compute Engine | Azure Virtual Machines | Instances | Public Cloud Instances |
| Managed Kubernetes | EKS | GKE | AKS | Kapsule | Managed Kubernetes Service |
| PaaS | AWS Elastic Beanstalk | App Engine | Azure App Service | - | Web PaaS |
| Containers without infrastructure | AWS AppRunner, AWS Fargate | Cloud Run | Azure Container Apps/Instance | Serverless Containers | - |
| Hybrid Container | AWS EKS AnyWhere | Anthos, GKE Enterprise | Azure Arc | - | - |
| Platform for rapid creation of web and mobile applications | AWS Amplify | Firebase | Visual Studio App Center | - | - |
| FaaS | AWS Lambda | Cloud Functions | Azure Functions Serverless Compute | Serverless Functions | - |
| Container Registry | Amazon ECR | Container Registry | Azure Container Registry | Container Registry | - |
| File Object storage | AWS Simple Storage Service (S3) | Cloud Storage (GCS) | Azure Blob Storage | Object Storage | Object Storage |
| Relational Database | AWS Relational Database Service (RDS), Aurora, Neptune | Cloud SQL, Cloud Spanner, AlloyDB | Azure Database for MySQL/PostgreSQL | Database for PostgreSQL/MySQL | Cloud Databases |
| SQL database migration | AWS Migration hub | Database Migration Service | Azure Database Migration Service | - | Database Migration Service |
| NoSQL | AWS DynamoDB, AWS DocumentDB | Firestore, Datastore, Bigtable | Azure Cosmos DB | - | MongoDB |
| In-Memory Data Storage | Amazon ElastiCache | Memorystore | Azure Cache | Database for Redis | Redis |
| Backups | AWS Backup | Cloud Storage Object Versioning and Lifecycle Management | Azure Backup | Backup services | Backup Storage |
| API Management | AWS API Gateway, AWS Publisher Service | API Gateway, Apigee API Management | Azure API Management | API Gateway | API Gateway |
| Cost Management | AWS Cost Explorer, AWS Budgets | Billing, FinOps Hub | Azure Cost Management | Billing | Control Panel Billing |
| Logging | CloudWatch Logs | Cloud Logging | Azure Monitoring Logs | Cockpit Logs | Logs Data Platform |
| Monitoring | CloudWatch | Cloud Monitoring | Azure Monitoring | Cockpit/Monitoring | Metrics |
| Audit logs | AWS CloudTrail | Cloud Audit Logs | Azure Audit Logs | - | Audit Logs |
| Tracing | AWS X-Ray | Cloud Trace | Azure Monitor Application Insights Distributed Tracing | - | - |
| Application Performance Monitoring | AWS X-Ray, CloudWatch Application Insights | Cloud Trace, Cloud Profiler | Azure Application Insights | - | - |
| CDN | Amazon CloudFront | Cloud CDN | Azure Content Delivery Network | - | CDN |
| Domains and DNS | Amazon Route 53 | Cloud Domains | Azure App Service | Domains and DNS | Domain Names |
| Virtual Private Cloud | AWS VPC | VPC | Azure Virtual Network | Private Networks/VPC | vRack |
| NAT gateway | AWS NAT gateway | Cloud NAT | Azure NAT Gateway | Public Gateway | - |
| Firewall | Security Group | Cloud Firewall | Azure Firewall | Security Groups | Network Security Groups |
| Web Application Firewall | AWS WAF | Google Cloud Armor | Azure Firewall | - | Web Application Firewall |
| DDoS Protection | AWS Shield | Google Cloud Armor Managed Protection Plus | Azure DDoS Protection | - | Anti-DDoS |
| Load Balancer | Elastic Load Balancer (ELB), Global Accelerator | Cloud Load Balancing | Azure Load Balancer | Load Balancer | Load Balancer |
| Direct Connect | AWS Direct Connect | Cloud Interconnect | Azure ExpressRoute | - | vRack Connect |
| Network Security | AWS Virtual Private Network (VPN) | Cloud VPN | Azure Virtual Private Network (VPN) | VPN | VPN |
| Private Link | AWS Private Link | Private Service Connect, VPC Service Controls | Azure Private Link | - | Private Link |
| Autoscaling | AWS EC2 Autoscaling | Compute Engine Autoscaler | Azure Autoscale, Azure Virtual Machine Scale Sets | - | Auto Scaling |
| Block storage for VMs | Amazon Elastic Block Store (EBS) | Persistent Disk | Azure Managed Disks | Block Storage | Additional Disks |
| Managed NFS Server | AWS Elastic File System (EFS), FSx | Filestore | Azure Files | Shared storage services | NAS-HA |
| Archive storage | AWS S3 Glacier | Cloud Storage Archive | Azure Archive Storage | Glacier | Cold Archive |
| Storage Transfer | AWS Storage Gateway, DataSync | Cloud Storage Transfer Service | Azure StorSimple | - | - |
| Email Service | Amazon SES | Gmail API, SendGrid | Azure Communication Services | Transactional Email | Email Pro |
| SMS/Communication | Amazon SNS, Pinpoint | - | Azure Communication Services | - | SMS API |
| Messaging | SNS, SQS, Amazon MQ | Pub/Sub | Azure Service Bus Messaging | Messaging and Queuing/SQS NATS | - |
| Asynchronous service requests | AWS EventBridge, AWS Notification Service (SNS) | Cloud Tasks | Azure Service Bus, Azure Storage Queues | - | - |
| Event Streaming | Amazon Kinesis, MSK | Pub/Sub | Azure Event Hubs | - | - |
| Data storage | Athena, Redshift | BigQuery | Azure Synapse Analytics | - | Analytics Data Platform |
| Query Service | Amazon Redshift Spectrum | BigQuery | Azure Synapse Analytics | - | - |
| Stream data processing | AWS Kinesis | Dataflow | Azure Stream Analytics | - | - |
| Stream data ingest | AWS Kinesis | Pub/Sub | Azure Events Hubs | - | - |
| Data workflow orchestration | Amazon Data Pipeline, AWS Glue | Cloud Composer | Azure Data Factory | - | - |
| Data processing | AWS Elastic MapReduce (EMR) | DataProc | Azure Data Lake Analytics, HDInsight | - | Data Processing |
| Data lake management and governance | AWS Lake Formation | Dataplex | Azure Purview | - | - |
| IoT Platform | AWS IoT Core | Cloud IoT Core | Azure IoT Hub | IoT Hub | - |
| Edge Computing | AWS Wavelength, Local Zones | Google Distributed Cloud Edge | Azure Stack Edge | Edge Services | - |
| AI & Machine Learning platform | AWS SageMaker, Bedrock | Vertex AI, Dialogflow | Azure AI Platform | - | AI Platform |
| AI & Machine Learning platform assistant | AWS SageMaker Autopilot | Vertex AI AutoML, Vertex AI custom training | AutoML, Azure Cognitive Services, Azure Machine Learning | - | - |
| Tensorflow | Tensorflow on AWS | TensorFlow Enterprise | Azure Databricks | - | - |
| Disaster Recovery | AWS Disaster Recovery | - | Azure Site Recovery | - | Disaster Recovery Plan |
| Identity and Access Management | IAM | IAM | Azure Active Directory External Identities | IAM | Identity and Access Management |
| CIAM | AWS Cognito | Identity Platform | Azure Active Directory B2C | - | - |
| Single Sign-On | AWS SSO (Identity Center) | Cloud Identity | Azure Active Directory | - | - |
| Config Management | AWS System Manager | Anthos Config Management | Azure App Configuration | - | - |
| Security and risk management platform | AWS Guard Duty, AWS Security Hub, AWS Audit Manager, AWS Config | Security Command Center | Microsoft Defender for Cloud | - | - |
| SIEM | AWS Security Lake | Chronicle | Azure Sentinel | - | - |
| Security assessment tool | AWS Inspector | Google Cloud Security Command Center (Cloud SCC), Google Cloud Security Scanner | Azure Security Center | - | - |
| Secret management | AWS Secrets Manager, AWS Systems Manager Parameter Store | Secret Manager | Azure Key Vault | Secret Manager | - |
| Key Management Service | AWS KMS | Cloud KMS | Azure Key Vault | - | Key Management Service |
| Hardware Security Module | AWS HSM | Cloud HSM | Azure Managed HSM | - | - |
| Certificate Management | AWS Certificate Manager (ACM) | Google Cloud SSL Certificates | Azure Key Vault | - | SSL Certificates |
| Resources management | AWS Organizations, Resource Groups & Tag Editor | Resource Manager | Azure Management Groups | Organizations | Projects |
| CI/CD | AWS CodeBuild, AWS CodeDeploy, AWS CodePipeline | Cloud Build | Azure DevOps, GitHub Enterprise | - | - |
| AI Companion | Amazon CodeWhisperer, Amazon Q | Duet AI, Gemini | Copilot | - | - |
| IaC Deployment | CloudFormation, CDK | Cloud Deployment Manager | Azure Deployment Manager | Terraform | Terraform |
| Security recommendations dashboard | Trusted Advisor | Security Command Center | Azure Advisor | - | - |
| Dashboard for monitoring the health of services | Health Dashboard, QuickSight | Google Cloud Status | Azure Service Health | Status Page | Status |
| Inventory of data assets | AWS Glue Data Catalog | Cloud Data Catalog | Azure Purview | - | - |
| Dedicated Servers | AWS Dedicated Hosts | Sole-tenant nodes | Azure Dedicated Host | Elastic Metal | Dedicated Servers |
| Serverless Database | Aurora Serverless | - | Azure SQL Database Serverless | Serverless SQL Database | - |
| Web Hosting | AWS Lightsail | - | Azure App Service | Web Hosting | Web Hosting |
| Trusted cloud (for France) | AWS European Sovereign Cloud (partnership with Germany) | S3NS (by Thales) | Bleu (by Capgemini & Orange) | SecNumCloud qualified | SecNumCloud qualified |


## Usefull links
* [AWS services](https://aws.amazon.com/?nc1=h_ls)
* [Azure services](https://azure.microsoft.com/en-gb)
* [GCP services](https://cloud.google.com/gcp/?hl=en)
* [Scaleway Documentation](https://www.scaleway.com/en/docs/)
* [OVHcloud Documentation](https://docs.ovh.com/gb/en/)
* [Google Cloud Platform Services Summary](https://cloud.google.com/terms/services?hl=en)
* [Google Documentation - Compare AWS and Azure services to Google Cloud](https://cloud.google.com/docs/get-started/aws-azure-gcp-service-comparison?hl=en)

## Pricing pages
* [AWS Pricing](https://aws.amazon.com/pricing/)
* [Azure Pricing](https://azure.microsoft.com/en-us/pricing/)
* [GCP Pricing](https://cloud.google.com/pricing)
* [Scaleway Pricing](https://www.scaleway.com/en/pricing/)
* [OVHcloud Pricing](https://www.ovhcloud.com/en/public-cloud/prices/)
