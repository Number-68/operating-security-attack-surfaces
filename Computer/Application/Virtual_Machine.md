todo: build virtual machine
# Virtual Machines

## What Is It?

A Virtual Machine (VM) is a software-defined computer that runs inside another computer.

A VM contains its own operating system, users, processes, services, networking, and applications while remaining isolated from the host machine through a hypervisor.

Common virtualization technologies include:

- KVM
- QEMU
- VirtualBox
- VMware
- Hyper-V

A VM functions much like a separate computer running on the same physical hardware.

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

- Host operating system
- Hypervisors
- Virtual hardware
- Networks
- Users
- Applications
- Storage devices
- Memory
- Process isolation mechanisms

---

## Why Does It Exist?

Virtual machines exist to provide strong isolation between workloads.

They allow users to:

- Run multiple operating systems
- Test untrusted software
- Separate workloads
- Perform malware analysis
- Create development environments
- Improve workload isolation
- Consolidate physical hardware

A VM provides a complete operating system environment without requiring another physical computer.

---

## Attack Surface

### How can an attacker interact with it?

Attackers may interact with virtual machines through:

- Vulnerable applications running inside the VM
- Exposed network services
- Shared folders
- Shared clipboard functionality
- Hypervisor vulnerabilities
- Misconfigured virtualization settings

### What does it expose?

Virtual machines may expose:

- Network services
- Applications
- Shared resources
- Virtual disks
- User accounts
- Host integration features

### What trust assumptions does it make?

- The hypervisor functions correctly.
- Isolation boundaries are properly enforced.
- Guest operating systems are secure.
- Shared resources are intentionally configured.
- Host and guest systems are trusted appropriately.

---

## Common Risks

- VM escape vulnerabilities
- Hypervisor vulnerabilities
- Exposed network services
- Vulnerable guest operating systems
- Excessive host integration
- Shared folder exposure
- Clipboard sharing abuse
- Misconfigured networking
- Outdated guest operating systems

---

## Defensive Controls

- Keep hypervisors updated.
- Keep guest operating systems updated.
- Disable unnecessary integration features.
- Limit shared folders.
- Restrict network access where appropriate.
- Use separate VMs for untrusted workloads.
- Follow the principle of least privilege.
- Monitor exposed services inside guest systems.

---

## Likelihood & Impact

### Likelihood

Moderate.

Virtual machines are widely used in enterprise environments, development workflows, server infrastructure, and security research. Their relevance depends heavily on how the system is used.

### Impact

High.

Properly configured VMs can significantly reduce risk by isolating workloads from one another.

However, vulnerabilities in the hypervisor or misconfigurations may weaken the intended isolation boundary and increase the impact of a compromise.

---

## Notes & Edge Cases

- Virtual machines provide stronger isolation than containers because they run their own operating systems and kernels.
- Virtual machines still rely on the security of the underlying hypervisor.
- A VM should not be considered invulnerable simply because it is isolated.
- Shared folders, shared clipboards, and device passthrough can weaken isolation.
- Virtual machines are commonly used as a containment strategy for risky software and experimentation.
- Not every workload requires a VM. Stronger isolation often comes at the cost of additional resource usage.
- VMs are best viewed as reducing trust assumptions between workloads rather than eliminating risk entirely.

# Personal Hardening Notes Summary

## Personal Device Setup

- Keep the hypervisor updated.
- Keep guest operating systems updated.
- Disable unnecessary host integration features.
- Limit shared folders between host and guest.
- Use dedicated VMs for untrusted software and experimentation.
- Use stronger isolation requirements as the risk of the workload increases.

## Personal Network Setup

- Restrict unnecessary network access to guest systems.
- Review exposed services inside virtual machines.
- Use isolated virtual networks when appropriate.
- Avoid exposing VM services to external networks unless required.

this is something just as passive. 
configuring and installing and maintaining and updating.
