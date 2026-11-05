# Users

## What Is It?

A user is an identity recognized by the operating system.

Users allow the system to distinguish between different people, services, and processes, and determine what actions they are allowed to perform.

Not all users represent actual people. Operating systems commonly create system users and service accounts used by applications and background services.

---

## Where Does It Sit?

- ❌ Physical World
- ❌ Hardware
- ❌ Firmware
- ✅ Kernel
- ✅ Userspace
- ❌ Network
- ❌ Cloud / External Systems

---

## What Does It Interact With?

- Groups
- Permissions
- Files and directories
- Processes
- Authentication systems
- Authorization systems
- Services
- Applications
- System resources

---

## Why Does It Exist?

Users exist to provide identity and accountability within an operating system.

They allow the system to:

- Identify who is performing an action
- Separate access between different users
- Control permissions and privileges
- Track ownership of files and processes
- Limit access to sensitive resources

Without users, every process would operate with the same identity and level of access.

---

## Attack Surface

### How can an attacker interact with it?

Attackers often attempt to gain access by compromising a user account.

Potential interaction points include:

- Login interfaces
- Stolen credentials
- Password guessing
- Social engineering
- Session hijacking
- Misconfigured accounts
- Privilege escalation

### What does it expose?

- User-owned files
- User permissions
- User processes
- Authentication methods
- Access to system resources

### What trust assumptions does it make?

- The authenticated user is who they claim to be.
- Users protect their credentials.
- User permissions are configured correctly.
- Applications act within the privileges of the user running them.

---

## Common Risks

- Weak passwords
- Reused passwords
- Excessive user privileges
- Shared accounts
- Dormant user accounts
- Credential theft
- Social engineering
- Privilege escalation
- Running everyday activities as an administrator

---

## Defensive Controls

- Use strong unique passwords.
- Enable multi-factor authentication when available.
- Remove unused accounts.
- Follow the principle of least privilege.
- Use separate administrator and standard accounts when appropriate.
- Monitor for unexpected account activity.
- Limit unnecessary access rights.

---

## Likelihood & Impact

### Likelihood

Very High.

Nearly every attack against a system eventually involves a user identity, whether through credential theft, impersonation, privilege escalation, or misuse of legitimate access.

### Impact

High.

Compromising a user account can grant access to files, applications, credentials, and other resources available to that user.

The level of impact depends on the privileges assigned to the account.

---

## Notes & Edge Cases

- Users are often considered a security boundary within the operating system.
- Many successful attacks target users rather than technical vulnerabilities.
- A compromised user account may be more valuable to an attacker than exploiting software vulnerabilities.
- System users and service accounts are users too, even though no person directly logs into them.
- User security is closely tied to authentication, authorization, groups, and permissions.
- The user account is often the first security identity an attacker attempts to obtain.

# Personal Hardening Notes Summary

Personal Device Setup
- Use a strong unique account password.
- Do not perform daily tasks as root.
- Use sudo only when necessary.
- Remove unused accounts.
- Review account privileges periodically.

Personal Network Setup
- N/A

Never use Root as a regular user. Always sudo from a wheel group user. Passwords too! Keep good passwords!