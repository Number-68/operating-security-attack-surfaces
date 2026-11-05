# Containers

## What Is It?

A container is an isolated environment used to run applications and services separately from the rest of the operating system.

Containers package software together with its dependencies while sharing the host system's kernel.

Common container technologies include:

- Docker
- Podman
- LXC/LXD
- Kubernetes (container orchestration)

Containers are often used to improve portability, consistency, and isolation.

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

- Processes
- Services
- Applications
- Filesystems
- Networks
- Users
- Permissions
- Operating system kernel
- Container runtimes

---

## Why Does It Exist?

Containers exist to isolate workloads and simplify software deployment.

They help:

- Reduce dependency conflicts
- Improve portability
- Isolate applications
- Simplify deployment
- Reduce operational complexity
- Limit the impact of compromised workloads

Containers allow software to run in a restricted environment without requiring a full virtual machine.

---

## Attack Surface

### How can an attacker interact with it?

Attackers may interact with containers through:

- Vulnerable applications running inside containers
- Misconfigured container permissions
- Exposed network services
- Container runtime vulnerabilities
- Shared resources between host and container

### What does it expose?

Containers may expose:

- Network services
- APIs
- Mounted filesystems
- Container images
- Container runtime interfaces
- Shared system resources

### What trust assumptions does it make?

- Container isolation functions correctly.
- Applications inside containers behave as expected.
- Container images are trustworthy.
- The host operating system is secure.
- Container permissions are configured correctly.

---

## Common Risks

- Overly privileged containers
- Vulnerable container images
- Exposed services
- Container escape vulnerabilities
- Insecure image sources
- Shared secret exposure
- Excessive filesystem access
- Excessive network access
- Misconfigured container runtimes

---

## Defensive Controls

- Follow the principle of least privilege.
- Use trusted container images.
- Remove unnecessary capabilities.
- Restrict filesystem access.
- Restrict network access.
- Keep container runtimes updated.
- Avoid running containers as root where practical.
- Review container permissions regularly.

---

## Likelihood & Impact

### Likelihood

Moderate.

Containers are increasingly common in development, server environments, and modern software deployment workflows.

For users who do not utilize containers, this attack surface may have little relevance.

### Impact

Moderate to High.

A properly configured container can limit the impact of a compromised application. However, misconfigurations or container escape vulnerabilities may allow attackers to access resources outside the intended isolation boundary.

---

## Notes & Edge Cases

- Containers are not virtual machines.
- Containers share the host kernel, making kernel security important.
- Containers are primarily an isolation technology rather than a security feature.
- While containers can improve security, they should not automatically be considered a security boundary.
- Many container security issues originate from misconfiguration rather than container technology itself.
- Containers and sandboxing share many similar security goals.
- A container should be viewed as reducing risk and limiting scope rather than providing complete isolation.

# Personal Hardening Notes Summary

Personal Device Setup
- Use trusted container images.
- Keep container runtimes updated.
- Avoid running containers as root when practical.
- Remove unused containers and images.
- Limit filesystem mounts to only what is required.
- Review container permissions before deployment.

Personal Network Setup
- Restrict unnecessary container network access.
- Do not expose container services unless required.
- Review published ports periodically.
- Separate trusted and untrusted workloads when practical.