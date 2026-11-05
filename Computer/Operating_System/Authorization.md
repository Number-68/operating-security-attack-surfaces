# Authorization

## What Is It?

Authorization is the process of determining what actions an authenticated user, process, service, or device is allowed to perform.

After authentication answers:

"Who are you?"

Authorization answers:

"What are you allowed to do?"

Authorization governs access to files, directories, devices, services, applications, system resources, and administrative functionality.

---

## Where Does It Sit?

- ❌ Physical World
- ❌ Hardware
- ❌ Firmware
- ✅ Kernel
- ✅ Userspace
- ✅ Network
- ✅ Cloud / External Systems

---

## What Does It Interact With?

- Users
- Groups
- Permissions
- Authentication systems
- Files and directories
- Services
- Processes
- Devices
- Applications
- Access control mechanisms

---

## Why Does It Exist?

Authorization exists to enforce access control after identity has been verified.

It helps systems:

- Restrict access to resources
- Enforce security policies
- Separate user privileges
- Protect sensitive information
- Limit damage from compromised accounts
- Implement the principle of least privilege

Without authorization, every authenticated user would have the same level of access.

---

## Attack Surface

### How can an attacker interact with it?

Attackers often interact with authorization systems after obtaining authenticated access to a system.

Common goals include:

- Accessing unauthorized resources
- Escalating privileges
- Bypassing access controls
- Abusing misconfigured permissions
- Leveraging excessive privileges

### What does it expose?

Authorization systems expose:

- Access control decisions
- Resource permissions
- User capabilities
- Administrative functions
- Security boundaries

### What trust assumptions does it make?

- Authentication correctly identified the user.
- Users have appropriate permissions.
- Access control rules are configured correctly.
- Resources are protected by the intended authorization mechanisms.
- Privileges are granted according to the principle of least privilege.

---

## Common Risks

- Excessive user privileges
- Misconfigured access controls
- Privilege escalation
- Unauthorized resource access
- Excessive service permissions
- Improper role assignments
- Inherited permissions that grant unnecessary access
- Failure to remove obsolete access

---

## Defensive Controls

- Follow the principle of least privilege.
- Regularly review user access.
- Audit permissions and access rights.
- Remove unnecessary privileges.
- Use role-based access controls where appropriate.
- Separate administrative and standard user activities.
- Review service account permissions periodically.

---

## Likelihood & Impact

### Likelihood

Very High.

Every operating system relies on authorization mechanisms to determine access to resources.

Misconfigured authorization controls are a common source of unintended access and privilege escalation opportunities.

### Impact

High.

Authorization failures can allow users, applications, or attackers to access resources beyond their intended permissions.

Successful abuse of authorization mechanisms often results in unauthorized access, privilege escalation, or compromise of sensitive data.

---

## Notes & Edge Cases

- Authentication and authorization are closely related but perform different functions.
- Authentication answers: "Who are you?"
- Authorization answers: "What are you allowed to do?"
- Authorization often relies on users, groups, permissions, and access control policies.
- A user can be successfully authenticated but still denied access to a resource.
- Many privilege escalation vulnerabilities are ultimately authorization failures.
- Authorization is one of the primary mechanisms used to enforce security boundaries within an operating system.

# Personal Hardening Notes Summary

Personal Device Setup
- Follow the principle of least privilege.
- Use standard user accounts for daily activities.
- Use sudo only when required.
- Review user and service permissions periodically.
- Remove access that is no longer needed.
- Separate administrative and everyday tasks when practical.

Personal Network Setup
- Restrict access to network services based on necessity.
- Apply least-privilege principles to remotely accessible accounts.

This is similar to the user entry. keep track of privileges and what users can do. Don't use sudo. This is not something that you need to monitor, but just practice.