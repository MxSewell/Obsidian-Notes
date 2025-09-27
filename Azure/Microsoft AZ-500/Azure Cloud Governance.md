Cloud Governance policies in Azure

Asset Management benchmarks:

1. Track asset inventory and their risks

2. Use only approved services

3. Ensure security of asset lifecycle management

4. Limit access to asset management

Azure Resource Manager
Azure RBAC
Azure Blueprints & Resource Locks

5. Use only approved applications in virtual machine


Backup and recovery benchmarks:

Protect backup and recovery data
Azure Backup
Data automatically encrypted using platform managed keys with 256-bit AES encryption
Option to use your own keys managed in Key Vault

Data protection benchmarks:

Monitor anomalies and threats targeting sensitive data

Decrypt sensitive data in transit
Against out of band attacks (such as traffic capture) using encryption
Enforce HTTPS and latest versions of TLS (v1.2 or later)
Use SSH and RDP
For file transfers, user SFTP/FTPS

Use a secure key management process
Use a secure certificate management process
Ensure security of key and certificate repository

Endpoint security benchmarks:

Use Endpoint Detection and Response (EDR)
Microsoft Defender
Microsoft Sentinel (SIEM solution)

Use modern anti-malware software

Ensure anti-malware software and signatures are updated

Governance and strategy benchmarks:

Define and implement security posture management
Define and implement multi-cloud security strategy

Identity management benchmarks:

Restrict exposure of credentials and secrets

Incident response benchmarks:

Detection and analysis - investigate incidents
Containment, eradication and recovery - automate the incident handling

Logging and threat detection benchmarks:

Enable threat detection capabilities
Enable logging for security investigation
Enable network logging for security investigation
Centralize security log management and analysis
Configure log storage retention
Azure activity logs are retained for 90 days then queued for deletion

Posture and vulnerability benchmarks:

Audit and enforce secure configurations for compute resources
Perform vulnerability assessments
Rapidly and automatically remediate vulnerabilities

Azure governance

Monitor > configure > govern > secure > protect > migrate

Azure Blueprints
Hub and spoke model
Azure landing zone

Azure Dedicated HSM
cryptographic key storage in Azure
FIPS 140-2 Level 3 compliant
Globally available across several Azure regions
Thales Luna 7 HSM model A790 appliances

Use a vault per application per environment
Individual keys, secrets, and certs should be used for specific scenarios
Key Vault manages X.509 certs
Key rotation
Key Vault will failover to a paired region automatically in the event of disaster

Microsoft Defender for Cloud

Malware scanning in real time

Streamline your organization’s threat detection and response capabilities by leveraging Microsoft Defender for Cloud and Microsoft Sentinel via configuring workflow automation, integrating data connectors, enabling analytics rules, and managing security alerts for efficient incident management.
