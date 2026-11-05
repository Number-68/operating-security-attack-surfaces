# Services

## What Is It?

A service is a program that runs in the background and performs a specific function for the operating system, applications, or users.

Services often start automatically and continue running without direct user interaction.

Examples include:

- SSH servers
- Printing services
- DNS resolvers
- Web servers
- Container runtimes
- Audio services
- Network management services

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

- Users
- Processes
- Applications
- Network interfaces
- Filesystems
- Devices
- Authentication systems
- Operating system resources

---

## Why Does It Exist?

Services exist to provide functionality that needs to remain available in the background.

They allow systems to:

- Respond to requests
- Manage hardware
- Provide networking functionality
- Handle authentication
- Run system tasks
- Support applications

Without services, many operating system features would require manual execution each time they were needed.

---

## Attack Surface

### How can an attacker interact with it?

Attackers often interact with services directly.

Potential interaction points include:

- Open network ports
- Local inter-process communication
- Misconfigurations
- Vulnerable software
- Excessive privileges
- Exposed service interfaces

### What does it expose?

Services may expose:

- Network ports
- APIs
- Local sockets
- Configuration interfaces
- Data access
- Administrative functionality

### What trust assumptions does it make?

- The service is configured correctly.
- Input received by the service is valid.
- The service only has the permissions it requires.
- Users interacting with the service are authorized.

---

## Common Risks

- Unnecessary running services
- Vulnerable services
- Services running as root
- Misconfigurations
- Weak authentication
- Exposed network ports
- Excessive privileges
- Default configurations
- Forgotten services

---

## Defensive Controls

- Disable unused services.
- Follow the principle of least privilege.
- Keep services updated.
- Restrict network exposure.
- Monitor running services.
- Review service configurations regularly.
- Use firewalls to limit access.
- Avoid running services as root when possible.

---

## Likelihood & Impact

### Likelihood

Very High.

Most systems run numerous services, many of which interact with users, applications, devices, and networks.

Services are one of the most common targets for attackers because they are often designed to accept input and perform actions.

### Impact

High.

A compromised service may provide access to sensitive information, system resources, network connectivity, or elevated privileges.

The impact depends heavily on the permissions and functionality available to the service.

---

## Notes & Edge Cases

- Many services never expose themselves to a network and operate entirely locally.
- A disabled service cannot generally be attacked through its normal interface.
- Services running with excessive privileges are often more dangerous than the service itself.
- The number of running services directly affects the size of a system's attack surface.
- A common security principle is: if a service is not needed, do not run it.
- Services are often the bridge between users, applications, and system resources.

# Personal Hardening Notes Summary

## Personal Device Setup

- Disable unused services.
- Review enabled services periodically.
- Keep service-related packages updated.
- Avoid running services as root when possible.
- Understand why a service is running before enabling it.

## Personal Network Setup

- Restrict network-facing services with a firewall.
- Only expose services that are required.
- Review listening ports periodically.

# Personal Hardening Notes Summary
Personal Device Setup
- Disable unused services.
- Review enabled services periodically.
- Keep service-related packages updated.
- Avoid running services as root when possible.
- Understand why a service is running before enabling it.

Personal Network Setup
- Restrict network-facing services with a firewall.
- Only expose services that are required.
- Review listening ports periodically.

This can be done directly, but it can also be made easier with other tools and services that are out there.
Monitoring service use is one of the main points. However, I am building an Arch Linux security stack. The less software, the less services, the less attack surfaces, the better.
I've had the notion in security and systems security that vulnerabilities comes from the complexity of things rather than things in general. Operating systems are seemingly easier to hack compared to a proprietary device with a specified, limited function.