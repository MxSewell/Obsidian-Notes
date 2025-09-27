
Managed identities are 
	fully managed by Microsoft Entra and can be used by Azure resources when accessing other Azure resources. Users need to manage passwords manually. Device is used for devices but cannot be used to access Azure resources. Service principal is used for apps, but not for Azure resources.

A service principal is, essentially,
	an identity for an application. For an application to delegate its identity and access functions to Microsoft Entra, the application must first be registered with Microsoft Entra to enable its integration. Once registered, a service principal is created in each Microsoft Entra tenant where the application is used.
