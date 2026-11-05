# Permissions

## What Is It?

Permissions are rules that determine what actions a user, group, or process is allowed to perform on a system resource.

They act as a security boundary between identities and resources by controlling who can read, write, modify, execute, or otherwise interact with files, directories, devices, services, and other system components.

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

- Users
- Groups
- Files and directories
- Processes
- Services
- Devices
- Authentication systems
- Authorization systems
- Access control mechanisms

---

## Why Does It Exist?

Permissions exist to restrict access to resources and prevent unauthorized actions.

They help:

- Protect sensitive data
- Separate users from one another
- Limit damage caused by compromised accounts
- Restrict services to necessary access
- Enforce the principle of least privilege
- Create security boundaries within the operating system

Without permissions, every user and process would have unrestricted access to all resources on the system.

---

## Attack Surface

### How can an attacker interact with it?

Attackers frequently interact with permissions after gaining access to a system.

Their goals often include:

- Reading sensitive files
- Modifying system resources
- Executing restricted actions
- Accessing other users' data
- Escalating privileges

### What does it expose?

Permissions expose what resources are accessible and what actions are allowed.

Examples include:

- File access
- Directory access
- Device access
- Service control
- Process interaction
- Administrative capabilities

### What trust assumptions does it make?

- Users have only the permissions they require.
- Permissions are configured correctly.
- Resources are assigned appropriate ownership.
- Applications operate within their assigned privileges.
- Administrators follow the principle of least privilege.

---

## Common Risks

- Overly permissive file permissions
- Excessive privileges
- Incorrect ownership assignments
- Misconfigured services
- World-readable sensitive files
- World-writable resources
- Privilege escalation opportunities
- Permission inheritance mistakes
- Unnecessary sudo access

---

## Defensive Controls

- Follow the principle of least privilege.
- Regularly review permissions and ownership.
- Limit administrative access.
- Restrict access to sensitive files.
- Audit permission changes periodically.
- Grant only the minimum access required.
- Remove unnecessary privileges when possible.

---

## Likelihood & Impact

### Likelihood

Very High.

Permissions are involved in nearly every interaction between users, services, processes, and resources within an operating system.

Misconfigured permissions are among the most common causes of unintended access.

### Impact

High.

Poorly configured permissions can allow unauthorized access to sensitive data, system resources, administrative functions, and other security boundaries.

Many privilege escalation paths rely on permission-related weaknesses.

---

## Notes & Edge Cases

- Permissions are one of the primary security boundaries within an operating system.
- Permissions and ownership work together to determine access.
- Correct permissions do not eliminate risk if a user's account is compromised.
- Excessive permissions often exist because it is easier to grant access than to manage it properly.
- Permissions answer the question: "What actions are allowed?"
- In Linux, common permissions include read (r), write (w), and execute (x), but modern systems may also implement Access Control Lists (ACLs) and additional access control mechanisms.
- Security is often improved more by removing unnecessary permissions than by adding new security tools.

# Personal Hardening Notes Summary

Personal Device Setup
- Follow the principle of least privilege.
- Review ownership and permissions periodically.
- Avoid excessive sudo usage.
- Restrict access to sensitive files.
- Audit permission changes when making major system modifications.
- Grant permissions only when required.

Similar to Groups and Users, keeping personal tabs on it is the bare minimum; however, still incredibly important.