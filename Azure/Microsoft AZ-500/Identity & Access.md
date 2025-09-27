
Manage security controls for identity and access

Cloud security benchmarks:
CIS Controls, NIST SP 800-53, & PCI-DSS ID standards

1. Use centralized identity and authentication system
2. Protect identity and authentication systems
3. Restrict privileged roles and accounts
4. Require strong authentication for all privileged access
5. Monitor and audit high risk activities
6. Manage application identities securely and automatically
7. Use managed application identities instead of creating human accounts for applications
8. Authenticate server and services
9. Enforce TLS to ensure connections to trusted servers and services
10. Single sign-on (SSO) for application access
11. Simple user experience for authenticating to resources
12. Use strong authentication controls
	1. Passwordless authentication or multi-factor authentication
	2. Passwords are deprecated as they are highly insecure
	3. Configure adminstrators and privileged users first
	4. Restrict resource access based on conditions

**Zero-trust access model**
Conditional based access:

1. Requiring MFA
2. Blocking sign-ins for users attempting to use legacy authentication methods
3. Requiring trusted locations for Entra ID MFA registration
4. Blocking risky sign-in behaviors
5. Requiring organization-managed devices for specific applications

**Principle of least privilege**
External identities

B2B Collaboration
Invite guest users to collaborate with your organization
Use identities from partner's identity management solution
Self-service sign-up

A tenant is a dedicated and trusted instance of Entra containing an org's resources
Workforce tenant, standard tenant
External tenant, exclusively for apps you want to publish to consumers and business customers

B2C Collaboration
Legacy solution

Microsoft Entra Connect

Password hash synchronization - in the cloud 
Pass-through synchronization - in the cloud, on-prem with same pwd
Federation integration - on-prem
Synchronization
Health Monitoring

Kerberos Authentication V5 Protocol
Kerberos Key Distribution Center (KDC)
Delegated authentication
SSO
Interoperability
More efficient to servers
Prior to Kerberos, NTLM authentication could be used, requiring an application server to connect to a DC
Kerberos allows renewable session tickets, thus replacing pass-through
Mutual authentication

Passwordless authentication
Something you have, know, are
Device + biometric or pin
Windows Hello, Authenticator, FIDO2 Passkeys, Certificates

Microsoft Entra Verified ID

Decentralized Identity
Decentralized Identifiers (DIDs)
Verifiable credentials

Management Groups
Subcriptions and organized and managed inside management groups
Management group > Subscription > Resource Group > Resource

Permissions management
Discover, remediate, monitor

Zero Trust
Assume Breach and verify each request as though it originated from an uncontrolled netowkr
Verify explicitly - Always authenticate and authorize based on all available data points
Least privilege - Limit user access with Just-In-Time and Just-Enough-Access (JIT/JEA)
Assume Breach - Minimize blast radius and segment access

--------------------------------------------------------------------------------------------------------------------

---------------------------------------------------------------------------------------------

Practice Test Notes

Privileged role administrators can manage PIM. 
Security administrators have permissions to manage security-related features.
Privileged authentication administrators can set or reset any authentication method, including passwords, for any user, including global administrators.

The Application Developer role has permissions to register an application even if the Users can register applications option is disabled.

To start using Entra Permission Management you first need to configure data collection from the Permission Management portal. This will enable you to onboard services such as Azure, AWS and Google Cloud. All other items can be configured after you enable data collection.

User Access Administrator is the least privileged role that grants access to Microsoft.Authorization/roleDefinition/write.

Resource Policy Contributor grants permissions to create and modify resource policy, create support ticket, and read resources and hierarchy. 

A permission allows the application to use a given API. A scope is used to request consent to run a given function on an API.

Using the Permission Creep Index is the most effective strategy to evaluate and adjust permissions regularly

The priority setting for a security rule can be a number between 100 and 4096. Rules are processed in priority order, with lower numbers processed before higher numbers, which results in lower numbers having a higher priority. 

You can associate an NSG to a virtual network subnet and network interface only. You can associate zero or one NSGs to each virtual network subnet and network interface on a virtual machine.

You can configure service endpoints for Azure Storage, Key Vault, and Azure SQL Database. You cannot configure service endpoints for virtual machines and Azure Firewall.

Rules can have a priority between 100 (highest priority) to 65,000 (lowest priority).

Implementing Azure Private Link allows secure access to Azure services over a private endpoint in your virtual network, ensuring that the applications are not exposed to the public internet. Setting up a VPN connection provides a secure tunnel for data transmission between on-premises networks and Microsoft Azure, allowing private access to applications without exposing them to the internet. Implementing Azure ExpressRoute provides a private connection between on-premises networks and Azure, but it does not inherently secure access to specific applications, making it unsuitable for the scenario's requirements.

CNI networking provides the best performance since it does not require IP forwarding and UDR, and ingress controllers can be managed from within Kuberbetes. Kubenet networking requires defined routes and IP forwarding, making the network slower. Azure load balancers cannot be managed by using Kubernetes tools.

Blob storage and Azure Files both support customer-managed keys. Azure Disk Storage, Azure NetApp Files, and Data Lake Storage do not support customer-managed keys.

Enabling Always Encrypted saves the encrypted data and only the client driver can decrypt it. TDE still allows users managing the database to see data.

The Subscription Owner role is the only role that has permissions to create and assign custom security initiatives in Defender for Cloud.

Key Vault Secrets User allows read access to secret content. Key Vault Crypto Officer allows   the user to perform actions on encryption keys, not secrets. Key Vault Reader allows the user to read the metadata of key vaults and its certificates, keys, and secrets, but not to read sensitive values, such as secret contents or key material.

Password policy enforcement can only be done using pass-through authentication
 Pass-through authentication with password hash sync meets the goals by enforcing on-premises password policies while providing backup authentication, all with minimal server infrastructure.

Federation requires server infrastructure and is overall more cumbersome to implement as a result

To enforce acceptance of the terms of use, you must create a Conditional Access policy.

Microsoft Entra supports JSON and CSV formats for a download

To produce reports with Log Analytics, first Microsoft Entra audit logs must be sent by using the Diagnostics settings.

Kusto Query Language (KQL)
1 min default smart lockout time
Only users can be owners of enterprise apps
Application permissions are used by apps that run without a signed-in user present, such as apps that run as background services or daemons. Only an administrator can consent to application permissions.

Delegated permissions are used by apps that have a signed-in user present. If an app performs a sign-in by using OpenID Connect, it must request the openid scope.

Access control and session policies need information to be updated in the Cloud Apps catalog.
Deleted user accounts are permanently removed from Microsoft Entra tenant automatically after 30 days. Restoring a user within the 30-day timeframe will also restore their license allocation and organization information.

MX & TXT records used to verify domain names
Dynamic user and dynamic device are the only two membership types that allow the use of dynamic membership rules to automatically add and remove members.

 SAML, or Security Assertion Markup Language, is an open standard XML-based framework that enables single sign-on (SSO) by facilitating the secure exchange of authentication and authorization data between an identity provider (IdP) and a service provider (SP). 
Client credentials flow and authorization code flow are both OAuth flows and are used for application authentication.

With entitlement management, you can collaborate with people outside your organization. To collaborate with users in an external Microsoft Entra tenant, you need to first add the users as a connected organization.

A program is a container that holds program controls. A tenant can have one or more programs. Each control links an access review to a program, to make it easier to locate related access reviews.

The first row of the CSV file used to perform a bulk invite must contain the version number.
Column headings are in the second line.

A custom RBAC role can be assigned at the resource, resource group, subscription, and management group level.
It cannot be assigned at the Microsoft Entra tenant level. Effectively, the largest supported scope is the management group.

Line-of-business applications, which are developed by the organization and not meant to be used by other companies.

Apps added through Microsoft Entra ID - App registrations are by default OIDC-based apps, while apps added through Microsoft Entra ID - Enterprise applications might use any SSO standard.