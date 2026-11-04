# TPM (Trusted Platform Module)

## What Is It?

A Trusted Platform Module (TPM) is a security-focused hardware component designed to securely store cryptographic keys, measurements, and other security-related information.

Its primary purpose is to provide a hardware root of trust for the system. Instead of storing sensitive secrets directly on disk, a TPM can protect them within hardware specifically designed for that purpose.

Modern systems may use a dedicated TPM chip or a firmware-based implementation such as Intel PTT or AMD fTPM.

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

- UEFI firmware
- Secure Boot
- Full Disk Encryption (e.g. LUKS, BitLocker)
- Operating system security services
- Authentication systems
- Cryptographic keys
- Boot process verification
- Hardware security features

---

## Why Does It Exist?

The TPM exists to establish trust between hardware, firmware, and the operating system.

It can be used to:

- Store cryptographic keys securely
- Support Full Disk Encryption
- Verify system integrity during boot
- Support device authentication
- Protect credentials and secrets
- Strengthen hardware-backed security

Without a TPM, many of these functions would rely entirely on software-based protection.

---

## Attack Surface

### How can an attacker interact with it?

An attacker typically interacts with a TPM indirectly through software, firmware, physical access, or attempts to bypass the security mechanisms that depend on it.

Potential interaction points include:

- Firmware configuration
- Boot process manipulation
- Operating system access
- Physical access attacks
- Vulnerabilities in TPM implementations
- Attacks against encryption workflows

### What does it expose?

- Hardware-backed key storage
- Platform integrity measurements
- Cryptographic services
- Authentication capabilities

### What trust assumptions does it make?

- Firmware is trustworthy.
- The boot chain has not been tampered with.
- Hardware has not been physically compromised.
- Keys stored within the TPM remain protected.
- The TPM implementation behaves as intended.

---

## Common Risks

- Firmware misconfiguration
- Physical access attacks
- TPM implementation vulnerabilities
- Secure Boot misconfiguration
- Loss of recovery keys
- Hardware tampering
- Improper encryption setup
- Reliance on TPM without recovery planning

---

## Defensive Controls

- Enable Full Disk Encryption.
- Keep firmware updated.
- Enable Secure Boot when appropriate.
- Store recovery keys securely.
- Use strong authentication methods.
- Restrict physical access to the device.
- Review firmware security settings periodically.

---

## Likelihood & Impact

### Likelihood

Low.

Most users are unlikely to encounter direct attacks against a TPM.

### Impact

High.

The TPM often protects critical security functions such as encryption keys, system integrity measurements, and authentication mechanisms. Misconfigurations or failures can affect the trustworthiness of the entire system.

---

## Notes & Edge Cases

- The TPM is not a security solution by itself. It is a building block used by other security technologies.
- A TPM does not prevent malware, phishing, or poor security practices.
- TPMs are commonly used alongside Secure Boot and Full Disk Encryption.
- Many modern systems implement TPM functionality through firmware rather than a dedicated chip.
- For most users, the TPM is rarely interacted with directly. Instead, users interact with the features built on top of it.
- The TPM is best viewed as a hardware root of trust rather than a traditional security application.

# Personal Hardening Notes Summary

Personal Device Setup
- Enable TPM support in firmware.
- Use TPM-backed Full Disk Encryption where practical.
- Store encryption recovery keys securely.
- Keep firmware updated.
- Review Secure Boot configuration.

Personal Network Setup
- N/A