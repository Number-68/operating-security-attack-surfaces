# Physical Access

## What Is It?

Physical access refers to a person's ability to directly interact with a computer, device, or hardware component in the real world.

Unlike network-based attacks, physical access allows an attacker to touch, modify, remove, inspect, or replace hardware directly.

Many security assumptions change once an attacker gains physical possession of a system.

---

## Where Does It Sit?

- ✅ Physical World
- ✅ Hardware
- ✅ Firmware
- ✅ Kernel
- ✅ Userspace
- ❌ Network
- ❌ Cloud / External Systems

---

## What Does It Interact With?

- The entire computer
- Storage devices
- USB devices
- BIOS & UEFI
- TPM
- Users
- Authentication systems
- Bootloaders
- Operating systems
- Firmware
- Peripheral devices

---

## Why Does It Exist?

Physical access is not a technology or feature.

It is a condition that exists whenever a person can directly interact with a device.

Because computers exist in the physical world, physical access is a fundamental consideration in system security.

---

## Attack Surface

### How can an attacker interact with it?

An attacker with physical access may be able to:

- Access the device directly
- Connect external devices
- Remove storage devices
- Modify firmware settings
- Boot from external media
- Install hardware implants
- Inspect hardware components
- Reset certain security settings

### What does it expose?

Physical access may expose:

- Storage devices
- Peripheral interfaces
- Firmware settings
- User sessions
- Authentication mechanisms
- Hardware components

### What trust assumptions does it make?

- Unauthorized individuals cannot access the device.
- Hardware has not been modified.
- Security controls remain intact.
- Physical security controls are functioning properly.
- Sensitive devices are not left unattended in hostile environments.

---

## Common Risks

- Device theft
- Unauthorized access to unlocked devices
- Evil Maid attacks
- Booting from external media
- Unauthorized USB devices
- Hardware tampering
- Firmware modification
- Storage device removal
- Shoulder surfing
- Physical observation of credentials

---

## Defensive Controls

- Use full disk encryption.
- Lock devices when unattended.
- Configure automatic screen locking.
- Use strong authentication mechanisms.
- Restrict physical access to systems.
- Enable firmware security features.
- Disable unnecessary external boot options.
- Maintain physical awareness of devices.

---

## Likelihood & Impact

### Likelihood

Moderate.

Many systems spend most of their time in trusted physical environments. However, laptops, mobile devices, public systems, and shared environments may face increased risk.

### Impact

Very High.

Physical access can bypass or weaken security assumptions that protect against remote attackers.

A physically compromised device may allow access to hardware, storage, firmware, and running sessions depending on the circumstances.

---

## Notes & Edge Cases

- A common security saying is: "Physical access is root access."
- Many operating system security controls assume physical access is already trusted.
- Full Disk Encryption significantly changes the threat model for stolen devices.
- Physical access does not automatically mean total compromise, but it often provides opportunities unavailable to remote attackers.
- Security should account for both technical threats and physical threats.
- Physical security is often the foundation upon which other security controls rely.
- Some attacks require no software vulnerability at all; they only require access to the device itself.
- There is a reason many servers are kept in locked rooms, racks, cages, or data centers. Physical access changes the threat model significantly.
- A lot of software security assumes an attacker cannot simply walk up to the machine and interact with it directly.
- Physical security is often the first wall protecting all of the software security behind it.


# Personal Hardening Notes Summary

Personal Device Setup

- Full Disk Encryption enabled.
- Automatic screen lock enabled.
- Lock device when unattended.
- Strong account password.
- Secure Boot enabled where practical.
- Review firmware security settings periodically.

Personal Network Setup
- N/A