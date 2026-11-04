# GPU (Graphics Processing Unit)

## What Is It?

A Graphics Processing Unit (GPU) is a hardware component responsible for rendering graphics, processing visual data, accelerating video playback, and performing parallel computations.

Modern GPUs are used for desktop rendering, gaming, video editing, machine learning workloads, scientific computing, and hardware acceleration throughout the operating system.

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

- Operating system graphics stack
- Applications
- Display devices
- GPU drivers
- Graphics APIs (OpenGL, Vulkan, etc.)
- Video acceleration services
- Firmware
- System memory

---

## Why Does It Exist?

The GPU exists to process graphical workloads more efficiently than a general-purpose CPU.

It is responsible for:

- Rendering desktop environments
- Gaming and 3D graphics
- Video playback and encoding
- Hardware acceleration
- Compute workloads
- Display output

Without a GPU, modern graphical interfaces would be significantly slower and less capable.

---

## Attack Surface

### How can an attacker interact with it?

Attackers typically interact with GPUs indirectly through software.

Potential interaction points include:

- Graphics drivers
- Browser rendering engines
- Graphics APIs
- Malicious applications
- Compute workloads
- Firmware vulnerabilities

### What does it expose?

- Driver interfaces
- Graphics APIs
- Hardware acceleration features
- Video memory
- Compute capabilities

### What trust assumptions does it make?

- Drivers behave correctly.
- Applications use graphics APIs safely.
- Firmware is trusted.
- Data provided to the GPU is handled securely.

---

## Common Risks

- Vulnerable graphics drivers
- Firmware vulnerabilities
- Privilege escalation through driver flaws
- Information leakage through shared resources
- Malicious applications exploiting GPU-related vulnerabilities
- Outdated driver packages

---

## Defensive Controls

- Keep GPU drivers updated.
- Keep the operating system updated.
- Use trusted repositories for graphics packages.
- Remove unused or unnecessary graphics drivers.
- Keep firmware updated when updates are available.

---

## Likelihood & Impact

### Likelihood

Low to Moderate.

Most attacks do not directly target the GPU. Attacks are more likely to target software and drivers that interact with it.

### Impact

Moderate to High.

Successful exploitation of graphics drivers can potentially lead to privilege escalation, information disclosure, or system compromise depending on the vulnerability.

---

## Notes & Edge Cases

- GPUs are generally maintenance-focused attack surfaces rather than actively managed ones.
- Most users do not need to perform extensive hardening beyond keeping drivers and software updated.
- The GPU itself is rarely the target. More commonly, vulnerabilities occur in the drivers, firmware, or software interacting with it.
- Browsers, games, desktop environments, and media applications all interact with the GPU regularly.
- For most personal systems, secure maintenance is typically more important than active hardening.

# Personal Hardening Notes Summary

Personal Device Setup
- Keep graphics drivers updated.
- Keep system packages updated.
- Use trusted repositories for graphics packages.
- Remove unused graphics drivers when practical.

Personal Network Setup
- N/A

Much more passive than having to actively harden it. Keep your devices updated and found vulnerabilities will be no issue.