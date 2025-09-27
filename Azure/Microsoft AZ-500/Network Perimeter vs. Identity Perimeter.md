Adopt a policy of **identity as the primary security perimeter**
Security perimeter has evolved from a network perimeter to an identity perimeter.
	*It doesn't matter what controls you have if a session can be stolen or your users fall victim to social engineering.*
Less concern about defending the network, more resources dedicated to defending data

PaaS deployment Identity Perimeter best practices

All keys/secrets should be stored in a centralized hardware security module (HSM) - Azure Key Vault
1. Don't put keys/secrets in source code or GitHub repositories
2. Manage VM access directly (SSH, RDP, etc.).
3. Multi-factor authentication
4. Use federated identities in Entra
5. Use commercial code over custom code
6. Use standard authentication protocols (OAuth/Kerberos)
7. Enable Azure DDoS protection on any perimeter virtual network

Azure App Service/API Management

Azure encryption models:
Server-side (service-managed, customer managed, & service managed in customer controlled hardware)
Client-side (performed outside of Azure - cloud provider doesn't have access to encryption keys)

Azure Storage Service Encryption (SSE) uses AES encryption, which is one of the strongest block ciphers available
AES handles encryption, decryption, and key management

**Key Vault** 

Data encrypted via Content Encryption Key (CEK) which is encrypted using a Key Encryption Key (KEK)
KEK can either be symmetric or asymmetric
S2S VPNs use IPsec for TLS encryption
Points of Precense (POP)

**Azure Bastion** 
provides secure RDP and SSH connectivity to all VMs in a virtual network in which it is provisioned
No public IP addresses or NSGs required

**Azure Kubernetes**
Containerization
Default Kubernetes lacks identity management solutions, therefore use Entra to manage identity
Create roles or ClusterRoles:
Azure Container Instances (ACIs)
Azure Container Apps (ACAs)
Azure Container Registry (ACR)

AKS clusters have local accounts enabled by default
az aks create > disable-local-accounts

Encryption at rest
Azure Disk Encryption/dm-crypt

Azure SQL Database/Azure SQL Managed Instance

**Microsoft Purview** for data governance and classification
Always Encrypted recommended for sensitive data in use, rest, and in transit
Transparent Database Encryption (TDE)
Dynamic data masking limits sensitive data exposure by masking it to nonprivileged users

Container Networking Interface (CNI)
**Shared Access Signatures** (SAS key)

Azure Blob and Files support customer managed keys