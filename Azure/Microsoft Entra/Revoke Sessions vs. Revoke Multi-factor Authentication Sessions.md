
- **Scope:** 
    
    Revoke sessions is a broad sign-out across all devices and apps, while Revoke MFA sessions is focused specifically on the MFA trust relationship for the user's devices. 
    
- **Effect on Session Token:** 
    
    Revoke sessions invalidates refresh tokens, but Revoke MFA sessions does not. 
    
- **Security vs. Usability:** 
    
    Revoke sessions provides a strong, immediate security response to a compromised account or device. Revoke MFA sessions is a middle ground that enhances security without completely disrupting the user's sessions by forcing a re-authentication of the MFA method itself.