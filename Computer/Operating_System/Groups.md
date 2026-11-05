# Groups

## What Is It?

A group is a collection of users that share a common set of permissions and access rights.

Instead of assigning permissions to every user individually, operating systems can assign permissions to a group and grant access to all members of that group.

Groups help simplify access control and privilege management.

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
- Permissions
- Files and directories
- Processes
- Devices
- Services
- Authentication systems
- Authorization systems

---

## Why Does It Exist?

Groups exist to simplify permission management.

Instead of configuring access for every user individually, administrators can place users into groups that have predefined access rights.

Groups help:

- Organize users
- Delegate permissions
- Control access to files and devices
- Limit administrative overhead
- Apply security policies consistently

---

## Attack Surface

### How can an attacker interact with it?

Attackers often benefit from group memberships once they gain access to a system.

Potential interaction points include:

- Compromised user accounts
- Privilege escalation
- Misconfigured group memberships
- Overly permissive group assignments
- Service account abuse

### What does it expose?

Groups may grant access to:

- Files and directories
- Devices
- Administrative functions
- Services
- System resources

The permissions available to a compromised account often depend heavily on its group memberships.

### What trust assumptions does it make?

- Users are assigned to appropriate groups.
- Groups contain only intended members.
- Permissions assigned to groups are reasonable.
- Administrators understand the privileges granted by each group.

---

## Common Risks

- Excessive group memberships
- Misconfigured permissions
- Unnecessary administrative access
- Forgotten users remaining in privileged groups
- Users inheriting permissions they do not need
- Service accounts belonging to overly privileged groups

---

## Defensive Controls

- Follow the principle of least privilege.
- Regularly review group memberships.
- Remove users from unnecessary groups.
- Minimize membership in administrative groups.
- Understand the permissions associated with each group.
- Periodically audit service accounts.

---

## Likelihood & Impact

### Likelihood

High.

Groups are used extensively throughout Linux and other operating systems to manage access and permissions.

Most systems depend on groups to enforce security boundaries.

### Impact

High.

Improper group assignments can grant access to files, devices, services, or administrative capabilities that users should not possess.

Many privilege escalation paths ultimately involve access that was unintentionally granted through group membership.

---

## Notes & Edge Cases

- Groups do not grant access by themselves; they work together with permissions and access control mechanisms.
- Some groups may grant surprisingly powerful capabilities.
- Users may belong to multiple groups at the same time.
- Service accounts often belong to specialized groups that control access to specific resources.
- Group memberships are a form of authorization rather than authentication.
- Groups answer the question: "What category of users does this account belong to?"

# Personal Hardening Notes Summary

Personal Device Setup
- Follow the principle of least privilege.
- Review group memberships periodically.
- Avoid unnecessary membership in privileged groups.
- Remove unused users from groups.
- Understand the privileges granted by groups before joining them.

Personal Network Setup
- N/A

Just like users's this is something to configure and doesn't need much passive external watchers. For this section, just have a image of what is going on, and remain vigilant. 