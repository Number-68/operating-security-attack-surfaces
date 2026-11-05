# Sandboxing

## What Is It?

Sandboxing is a security technique that isolates applications, processes, or workloads from the rest of the system.

The goal is to limit what a piece of software can access, even if it becomes compromised or behaves maliciously.

A sandbox acts as a controlled environment with restricted access to files, devices, network resources, and other system components.

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
- Users
- Permissions
- Filesystems
- Devices
- Network resources
- Operating system security mechanisms
- Containers and virtualization technologies

---

## Why Does It Exist?

Sandboxing exists to reduce the impact of compromised or untrusted software.

Rather than assuming all software is trustworthy, sandboxing assumes that software may eventually fail, become vulnerable, or be compromised.

Its purpose is to:

- Restrict access to sensitive resources
- Limit damage from security incidents
- Isolate applications from one another
- Reduce lateral movement within a system
- Create additional security boundaries

---

## Attack Surface

### How can an attacker interact with it?

Attackers typically interact with a sandbox by attempting to:

- Escape the sandbox
- Abuse permissions granted to the sandbox
- Exploit vulnerabilities in isolation mechanisms
- Access resources intentionally exposed to the sandbox

### What does it expose?

Sandboxes expose only the resources explicitly granted to them.

Examples include:

- Specific files and directories
- Devices
- Network access
- Hardware resources
- User data

### What trust assumptions does it make?

- The sandbox implementation functions correctly.
- Isolation boundaries are properly enforced.
- Applications only receive permissions they require.
- Kernel security mechanisms remain intact.
- Administrators properly configure access controls.

---

## Common Risks

- Overly permissive sandbox configurations
- Sandbox escape vulnerabilities
- Excessive filesystem access
- Excessive device access
- Excessive network access
- Weak isolation boundaries
- Misconfigured permissions
- Users granting unnecessary access

---

## Defensive Controls

- Follow the principle of least privilege.
- Grant only required permissions.
- Review sandbox permissions regularly.
- Keep sandboxing software updated.
- Remove unnecessary filesystem access.
- Remove unnecessary device access.
- Remove unnecessary network access.
- Prefer isolated application environments where practical.

---

## Likelihood & Impact

### Likelihood

Moderate.

Sandboxes themselves are not frequently attacked directly, but they often become relevant after another vulnerability has already been exploited.

### Impact

High.

A properly configured sandbox can significantly reduce the impact of a compromised application.

Conversely, a sandbox escape can allow an attacker to move beyond intended security boundaries and access additional resources.

---

## Notes & Edge Cases

- Sandboxing is primarily a defensive control rather than an attack surface.
- The purpose of a sandbox is containment, not prevention.
- Sandboxing assumes that applications may eventually become compromised.
- A weak sandbox may provide a false sense of security.
- Most modern operating systems use some form of sandboxing internally.
- Common examples include Flatpak, Firejail, Docker, Podman, browser sandboxes, AppArmor, and SELinux.
- Sandboxing is an example of defense-in-depth. Even if one security layer fails, additional boundaries may still limit the attacker's capabilities.
- A sandbox should be viewed as reducing risk rather than eliminating it.

# Personal Hardening Notes Summary

Personal Device Setup
- Use sandboxed applications when practical.
- Prefer Flatpak for untrusted desktop applications.
- Review application permissions periodically.
- Remove unnecessary filesystem access.
- Remove unnecessary device access.
- Keep sandboxing tools updated.
- Consider AppArmor or SELinux where appropriate.

Personal Network Setup
- Restrict unnecessary network access for sandboxed applications.
- Review network permissions granted to applications.

This is a solution. A defence control.