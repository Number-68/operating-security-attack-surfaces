# Device Firmware

## What Is It?

Device firmware is software embedded directly into hardware devices that allows them to function and communicate with the rest of the system.

Unlike normal applications, firmware runs on the device itself rather than on the operating system.

Examples include firmware found in:

- SSDs and HDDs
- Wi‑Fi adapters
- Bluetooth adapters
- GPUs
- USB controllers
- Keyboards
- Mice
- Monitors
- Routers
- Network cards

---

## Where Does It Sit?

- ❌ Physical World
- ✅ Hardware
- ✅ Firmware
- ❌ Kernel
- ❌ Userspace
- ❌ Network
- ❌ Cloud / External Systems

---

## What Does It Interact With?

- Hardware devices
- Device drivers
- Operating systems
- Motherboard firmware
- Users
- Applications (indirectly)
- Other hardware components

---

## Why Does It Exist?

Device firmware exists to provide low-level control and instructions that allow hardware devices to operate.

Without firmware, many hardware components would not know how to:

- Initialize themselves
- Process commands
- Communicate with the operating system
- Perform their intended functions

Firmware acts as the bridge between hardware and software.

---

## Attack Surface

### How can an attacker interact with it?

Attackers typically interact with device firmware indirectly through:

- Firmware update mechanisms
- Vulnerable device drivers
- Administrative system access
- Physical access
- Vendor software
- Hardware-specific vulnerabilities

### What does it expose?

- Device functionality
- Firmware update processes
- Hardware features
- Communication interfaces

### What trust assumptions does it make?

- Firmware has not been maliciously modified.
- Firmware updates come from trusted sources.
- Hardware behaves according to specifications.
- Drivers communicate with devices correctly.

---

## Common Risks

- Outdated firmware
- Firmware vulnerabilities
- Malicious firmware modifications
- Compromised update processes
- Vendor software vulnerabilities
- Supply chain concerns
- Poorly maintained hardware

---

## Defensive Controls

- Keep device firmware updated.
- Obtain firmware updates from trusted vendors.
- Remove unsupported or abandoned hardware when practical.
- Keep operating system and drivers updated.
- Restrict physical access to devices.
- Verify firmware updates before installation when possible.

---

## Likelihood & Impact

### Likelihood

Low.

Most attacks do not directly target device firmware. Software, applications, and users remain significantly more common targets.

### Impact

High.

Firmware often exists below the operating system's normal visibility and control mechanisms. A compromised device firmware can potentially undermine trust in the affected hardware component.

---

## Notes & Edge Cases

- Many users are unaware that their hardware devices contain firmware.
- Device firmware is often updated far less frequently than operating systems or applications.
- Most device firmware vulnerabilities are addressed through vendor updates.
- Some devices may never receive firmware updates after purchase.
- The majority of users will spend far more time maintaining software than device firmware.
- Device firmware sits between hardware and software, making it an important trust boundary.
- Firmware attacks exist, but for most users they are significantly less common than phishing, malware, misconfigurations, or application vulnerabilities.

# Personal Hardening Notes Summary

Personal Device Setup
- Keep device firmware updated when updates are available.
- Obtain firmware updates from trusted vendors.
- Keep device drivers updated.
- Replace unsupported hardware when practical.

Personal Network Setup
- N/A

Summary, just passive maintenance is all you can really do.