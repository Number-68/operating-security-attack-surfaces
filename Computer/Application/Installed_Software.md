# Installed Software

## What Is It?

Installed software refers to applications, utilities, tools, and programs that have been added to a system by the user, package manager, operating system, or third parties.

Installed software extends the capabilities of a computer by providing functionality beyond what is included in the base operating system.

Examples include:

- Media players
- Office applications
- Development tools
- Communication software
- Games
- System utilities
- Third-party applications

---

## Where Does It Sit?

- ❌ Physical World
- ❌ Hardware
- ❌ Firmware
- ❌ Kernel
- ✅ Userspace
- ✅ Network
- ✅ Cloud / External Systems

---

## What Does It Interact With?

- Users
- Filesystems
- Processes
- Services
- Network resources
- Hardware devices
- Browsers
- Authentication systems
- Operating system APIs

---

## Why Does It Exist?

Installed software exists to perform tasks and provide functionality that users need.

Examples include:

- Productivity
- Entertainment
- Development
- Communication
- Content creation
- System management

Most software is installed to solve a problem or provide a capability that the base operating system does not provide by itself.

---

## Attack Surface

### How can an attacker interact with it?

Attackers may interact with installed software through:

- Software vulnerabilities
- Malicious software updates
- Malicious plugins or extensions
- Misconfigurations
- User interaction
- Network communication
- File handling

### What does it expose?

Installed software may expose:

- Files
- User data
- Services
- Network connections
- APIs
- Credentials
- Permissions granted by the user

### What trust assumptions does it make?

- The software publisher is trustworthy.
- The software has not been tampered with.
- Updates originate from legitimate sources.
- The software only performs intended actions.
- Permissions granted to the application are appropriate.

---

## Common Risks

- Unpatched vulnerabilities
- Malware
- Supply chain attacks
- Malicious software downloads
- Excessive permissions
- Untrusted software sources
- Abandoned software
- Insecure plugins or extensions
- Unnecessary software installation

---

## Defensive Controls

- Install software only from trusted sources.
- Keep software updated.
- Remove unused applications.
- Review application permissions.
- Verify software authenticity when possible.
- Limit unnecessary software installations.
- Use sandboxing where practical.
- Monitor software that receives elevated privileges.

---

## Likelihood & Impact

### Likelihood

Very High.

Most users interact with installed software every day, and every installed application introduces additional complexity and potential attack surface.

### Impact

High.

Compromised software may access user data, interact with system resources, communicate over networks, or execute malicious actions depending on its permissions and capabilities.

The impact often depends on what privileges the software has been granted.

---

## Notes & Edge Cases

- Every installed application expands the system's attack surface to some degree.
- More software generally means more potential vulnerabilities, more updates, and more trust relationships.
- Many successful attacks target commonly used software rather than the operating system itself.
- Supply chain attacks can affect trusted software distributors and update mechanisms.
- Unused software can still represent a risk if it remains installed and unmaintained.
- A useful security principle is: if you do not need software, do not install it.
- Installed software often inherits the permissions and access rights of the user running it.

# Personal Hardening Notes Summary

Personal Device Setup
- Install software only when needed.
- Prefer trusted repositories and trusted software vendors.
- Keep applications updated.
- Remove unused software periodically.
- Review application permissions.
- Avoid running software as root unless necessary.
- Use sandboxing for untrusted applications when practical.

Personal Network Setup
- Restrict unnecessary network-facing applications.
- Review software that exposes ports or services.
- Use firewalls to limit application exposure where appropriate.