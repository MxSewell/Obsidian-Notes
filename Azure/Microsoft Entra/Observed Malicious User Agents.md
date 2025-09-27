
Axios 1.8.4 - Proofpoint researchers found that a recent campaign using the unique HTTP client Axios had an especially high success rate, compromising 43% of targeted user accounts. 

Python-Request - During this time, newly observed HTTP clients, like 'python-request,' were being integrated into brute force attack chains, significantly increasing threat volume and diversity. In May 2024, these attacks peaked, leveraging millions of hijacked residential IPs to target cloud accounts. 

BAV2ROPC (Basic Authentication Version 2 Resource Owner Password Credential) - authenticating by only validating username and password called basic authentication. Legacy protocol used to bypass MFA. Is commonly used by old email apps such as iOS Mail. It is often seen in SaaS/email account compromises where accounts have ‘legacy authentication’ enabled. This is because, even if multi-factor authentication (MFA) is activated, legacy protocols like IMAP/POP3 are not configured for MFA and so do not result in an MFA notification being sent.

Block MFA CA policy blocks legacy authentication. CA policies apparently are not applicable when sign-ins are conducted with legacy auth protocols.

Apps using their own legacy methods to authenticate with Microsoft Entra and access company data pose another risk for organizations. Examples of apps using legacy authentication are POP3, IMAP4, or SMTP clients. Legacy authentication apps authenticate on behalf of the user and prevent Azure AD from doing advanced security evaluations. The alternative, modern authentication, reduces security risk by supporting MFA and Conditional Access.