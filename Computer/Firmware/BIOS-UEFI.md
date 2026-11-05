# BIOS & UEFI

## What Is It?

BIOS (Basic Input/Output System) and UEFI (Unified Extensible Firmware Interface) are firmware systems responsible for initializing hardware and starting the operating system during the boot process.

Historically, computers used BIOS. Modern computers primarily use UEFI, which is the successor to BIOS and provides additional functionality and security features.

Although they are technically different, many people still refer to UEFI as "the BIOS" because both serve a similar role in the system.

---

## Where Does It Sit?

- ❌ Physical World
- ❌ Hardware
- ✅ Firmware
- ❌ Kernel
- ❌ Userspace
- ❌ Network
- ❌ Cloud / External Systems

---

## What Does It Interact With?

- CPU
- RAM
- TPM
- Storage devices
- Motherboard components
- Bootloaders
- Operating systems
- Secure Boot
- Hardware initialization processes

---

## Why Does It Exist?

BIOS and UEFI exist to prepare a computer for operation before the operating system loads.

Their responsibilities include:

- Initializing hardware
- Detecting connected devices
- Managing boot order
- Loading bootloaders
- Providing firmware configuration settings
- Establishing part of the system's trust chain

Without firmware, the computer would be unable to start the operating system.

---

## Attack Surface

### How can an attacker interact with it?

Attackers typically interact with BIOS/UEFI through:

- Physical access to the computer
- Firmware update mechanisms
- Administrative access to the operating system
- Firmware vulnerabilities
- Misconfigured firmware settings

### What does it expose?

- Hardware configuration settings
- Boot settings
- Firmware update interfaces
- Security features
- Device initialization processes

### What trust assumptions does it make?

- The firmware has not been modified maliciously.
- Hardware components are trustworthy.
- Firmware updates are legitimate.
- The boot process has not been tampered with.
- Administrative access is restricted to authorized users.

---

## Common Risks

- Firmware vulnerabilities
- Outdated firmware
- Insecure boot configurations
- Unauthorized firmware modification
- Weak or missing firmware passwords
- Boot order manipulation
- Physical access attacks
- Disabled security features
- Misconfigured Secure Boot settings

---

## Defensive Controls

- Keep firmware updated.
- Enable Secure Boot where practical.
- Restrict physical access to the system.
- Configure firmware passwords if appropriate.
- Disable unnecessary boot devices.
- Review firmware settings periodically.
- Use Full Disk Encryption alongside firmware protections.

---

## Likelihood & Impact

### Likelihood

Low.

Firmware-level attacks are relatively uncommon compared to attacks against applications, operating systems, or network services.

### Impact

Very High.

BIOS and UEFI sit beneath the operating system in the system's trust chain. A successful compromise at this level may affect the integrity of everything that loads afterward.

Because firmware runs before the operating system, it has significant control over the boot process.

---

## Notes & Edge Cases

- Traditional BIOS and modern UEFI are separate technologies, but both fulfill the role of system firmware.
- Most modern computers use UEFI rather than legacy BIOS.
- Many people use the term "BIOS" when referring to UEFI settings and firmware.
- UEFI introduces features not available in traditional BIOS, including Secure Boot support and more advanced boot management.
- BIOS & UEFI work closely with TPMs, bootloaders, and Full Disk Encryption solutions.
- Firmware security is often overlooked because users interact with it infrequently.
- The firmware layer forms a foundational trust boundary for the operating system.

# Personal Hardening Notes Summary

Personal Device Setup
- Keep motherboard firmware updated.
- Enable Secure Boot where practical.
- Review firmware settings after updates.
- Disable unnecessary boot devices.
- Use Full Disk Encryption.
- Configure firmware password if needed.

Concluding, basically: secure boot, knowing all boot devices, full disk encryption, and configuring your firmware password.