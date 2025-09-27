Sign-in/User Risk Conditional Access

The message "Require Authentication strength - Multifactor authentication: The user has satisfied this authentication strength" indicates that the user has successfully completed multifactor authentication (MFA) and the required authentication strength for accessing the resource or application has been met.

This means the user has provided two or more verification factors, such as a password and a code from a mobile app, to prove their identity and gain access. 

Example:
Imagine a user is trying to access a sensitive application within an organization. A Conditional Access policy is configured to require MFA with a phishing-resistant method like FIDO2 security key. The user has successfully authenticated using their FIDO2 key. The message "Require Authentication strength - Multifactor authentication: The user has satisfied this authentication strength" would be displayed because the user has met the required authentication strength. 

Policy Evaluation:

https://learn.microsoft.com/en-us/entra/identity/conditional-access/concept-conditional-access-report-only

Report-only: Success	All configured policy conditions, required non-interactive grant controls, and session controls were satisfied. For example, a multifactor authentication requirement is satisfied by an MFA claim already present in the token, or a compliant device policy is satisfied by performing a device check on a compliant device.

Report-only: Failure	All configured policy conditions were satisfied but not all the required non-interactive grant controls or session controls were satisfied. For example, a policy applies to a user where a block control is configured, or a device fails a compliant device policy.

Report-only: User action required	All configured policy conditions were satisfied but user action would be required to satisfy the required grant controls or session controls. With report-only mode, the user isn't prompted to satisfy the required controls. For example, users aren't prompted for multifactor authentication challenges or terms of use.

Report-only: Not applied	Not all configured policy conditions were satisfied. For example, the user is excluded from the policy or the policy only applies to certain trusted named locations.

Further observations:

User risk will only work optimally if SSPR is enabled tenant wide. It will also require that majority of our users are enrolled in MFA. 

Users seem to be able to self-remediate via mysignins.microsoft.com, which more than likely can be accessed via myaccount.microsoft.com
