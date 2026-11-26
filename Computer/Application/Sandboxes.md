# Sandboxing

## What Is It?

Sandboxing is a security technique used to restrict what an application, process, or service can access on a system.

A sandbox creates boundaries around software and limits access to files, devices, network resources, system calls, and other sensitive areas of the operating system.

Common sandboxing technologies include:

- Flatpak
- Firejail
- AppArmor
- SELinux
- Browser Sandboxes
- Operating System Isolation Mechanisms

Sandboxing is often used to reduce the damage caused by compromised or untrusted software.

---

## Where Does It Sit?

- ❌ Physical World
- ❌ Hardware
- ❌ Firmware
- ✅ Kernel
- ✅ Userspace
- ✅ Network
- ❌ Cloud / External Systems

---

## What Does It Interact With?

- Processes
- Applications
- Filesystems
- Network resources
- Devices
- Permissions
- Users
- Services
- Security policies
- Operating system isolation mechanisms

---

## Why Does It Exist?

Sandboxing exists to limit what software can do.

Rather than assuming software is always trustworthy, sandboxing assumes that applications may eventually become compromised, vulnerable, or malicious.

It helps:

- Restrict filesystem access
- Restrict device access
- Restrict network access
- Reduce attack impact
- Prevent unnecessary privilege exposure
- Create additional security boundaries

Sandboxing is designed to contain failures rather than prevent them entirely.

---

## Attack Surface

### How can an attacker interact with it?

Attackers typically interact with sandboxes by attempting to:

- Escape sandbox restrictions
- Abuse granted permissions
- Exploit sandbox vulnerabilities
- Access resources intentionally exposed to the sandbox
- Exploit weaknesses in isolation mechanisms

### What does it expose?

Sandboxes may expose:

- Approved files and directories
- Approved devices
- Approved network resources
- User-approved permissions
- Application-specific resources

### What trust assumptions does it make?

- The sandbox implementation functions correctly.
- Isolation boundaries are properly enforced.
- Applications only receive permissions they require.
- The operating system remains secure.
- Users understand the permissions they grant.

---

## Common Risks

- Overly permissive sandbox configurations
- Sandbox escape vulnerabilities
- Excessive filesystem access
- Excessive device permissions
- Excessive network permissions
- Misconfigured security policies
- Users granting unnecessary access
- False assumptions about isolation strength

---

## Defensive Controls

- Follow the principle of least privilege.
- Grant only required permissions.
- Review sandbox permissions regularly.
- Restrict filesystem access.
- Restrict device access.
- Restrict network access.
- Keep sandboxing tools updated.
- Remove unnecessary permissions and exceptions.

---

## Likelihood & Impact

### Likelihood

Moderate.

Most modern operating systems and applications use some form of sandboxing, though many users are unaware of it.

Direct attacks against sandboxing mechanisms are less common than attacks against users or applications.

### Impact

High.

A properly configured sandbox can significantly reduce the impact of a compromised application.

Conversely, a sandbox escape may allow an attacker to move beyond the intended security boundary and gain access to additional system resources.

---

## Notes & Edge Cases

- Sandboxing is primarily a defensive control rather than an attack surface.
- Sandboxing assumes that applications may eventually fail or become compromised.
- Sandboxes reduce risk but do not eliminate it.
- Containers and sandboxes share similar goals but solve different problems.
- A sandbox focuses on restricting permissions and access.
- A container focuses on packaging and isolating workloads.
- A virtual machine focuses on isolating an entire operating system.
- A weakly configured sandbox may provide a false sense of security.
- Sandboxing is best viewed as another layer in a defense-in-depth strategy.

# Personal Hardening Notes Summary

## Personal Device Setup

- Prefer sandboxed applications when practical.
- Review sandbox permissions periodically.
- Remove unnecessary filesystem access.
- Remove unnecessary device access.
- Remove unnecessary network access.
- Keep sandboxing tools updated.
- Prefer least-privilege configurations.

## Personal Network Setup

- Restrict network access for applications that do not require it.
- Review application network permissions periodically.

In my opinion, this is pretty passive as well. just have a sandboxer, and keep it updated? 