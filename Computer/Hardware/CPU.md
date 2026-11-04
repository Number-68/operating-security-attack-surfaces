# CPU (Central Processing Unit)

## What Is It?

A Central Processing Unit (CPU) is the primary processor responsible for executing instructions and performing computations on a computer.

It is often referred to as the "brain" of the computer because nearly every operation performed by the operating system and applications ultimately runs through the CPU.

---

## Where Does It Sit?

- ❌ Physical World
- ✅ Hardware
- ✅ Firmware
- ✅ Kernel
- ✅ Userspace
- ❌ Network
- ❌ Cloud / External Systems

---

## What Does It Interact With?

- Operating system kernel
- Applications
- System memory (RAM)
- Storage devices
- Hardware components
- Firmware
- Virtual machines
- Security features and mitigations

---

## Why Does It Exist?

The CPU exists to execute instructions and process data.

It is responsible for:

- Running the operating system
- Executing applications
- Managing computations
- Processing system instructions
- Coordinating interactions between hardware and software
- Supporting virtualization and security features

Without a CPU, the computer cannot function.

---

## Attack Surface

### How can an attacker interact with it?

Attackers typically interact with CPUs indirectly through software, operating systems, applications, or virtualization technologies.

Potential interaction points include:

- Application code
- Operating system workloads
- Virtual machines
- Browser-executed code
- Kernel operations
- CPU features and instruction sets

### What does it expose?

- Processing capabilities
- Hardware features
- Virtualization extensions
- Security extensions
- Shared computational resources

### What trust assumptions does it make?

- Software follows expected execution rules.
- Memory isolation functions correctly.
- CPU security features behave as designed.
- Microcode and firmware are trusted.
- Applications cannot improperly access protected resources.

---

## Common Risks

- CPU vulnerabilities (e.g., speculative execution attacks)
- Side-channel attacks
- Privilege escalation
- Information disclosure
- Microcode vulnerabilities
- Virtualization-related vulnerabilities
- Shared resource leakage between processes

---

## Defensive Controls

- Keep system packages updated.
- Install CPU microcode updates.
- Keep firmware updated.
- Enable operating system security mitigations.
- Use virtualization and isolation features when appropriate.
- Follow vendor security advisories.

---

## Likelihood & Impact

### Likelihood

Low to Moderate.

Most users will never encounter an attack targeting the CPU directly. CPU-related vulnerabilities are relatively uncommon compared to software and network-based attacks.

### Impact

High.

CPU vulnerabilities can potentially affect the fundamental security boundaries of a system because the CPU sits beneath nearly every layer of software.

Successful exploitation may result in information disclosure, privilege escalation, or bypassing security controls.

---

## Notes & Edge Cases

- Most CPU security issues are discovered by researchers rather than exploited through everyday attacks.
- The majority of CPU security is handled through microcode updates, firmware updates, kernel mitigations, and operating system patches.
- Unlike attack surfaces such as Wi‑Fi, USB, or SSH, users typically have few direct hardening options beyond staying updated.
- CPUs contain numerous security-related features such as virtualization extensions, execution protections, and hardware isolation mechanisms.
- The CPU is generally a maintenance-focused attack surface rather than an actively managed one.

# Personal Hardening Notes Summary

Personal Device Setup
- Keep system updated.
- Keep CPU microcode updated.
- Keep firmware updated.

Personal Network Setup
- N/A

Similar passive hardening.