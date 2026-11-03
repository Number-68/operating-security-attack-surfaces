# Storage Devices

## What Is It?

A storage device is hardware responsible for persistently storing data on a computer.

Examples include:

- SSDs
- Hard Disk Drives (HDDs)
- NVMe drives
- USB storage devices
- SD cards
- External drives

Unlike RAM, storage devices retain data even when the system is powered off.

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

- Operating system
- Filesystems
- Applications
- Users
- Permissions
- Encryption systems
- Physical hardware buses (SATA, NVMe, USB)

---

## Why Does It Exist?

Storage devices exist to persist information.

Without storage, a computer would lose:

- User files
- Applications
- Operating system data
- Configuration files
- Credentials
- Logs
- Encryption keys stored on disk

every time the machine powers off.

---

## Attack Surface

### How can an attacker interact with it?

Attackers may interact with storage devices through:

- The operating system
- Applications
- Physical access
- External storage interfaces
- Direct drive access
- Filesystem manipulation

### What does it expose?

- User data
- Configuration files
- Credentials
- Browser data
- Application data
- System logs
- Encryption metadata

### What trust assumptions does it make?

- Authorized users can access appropriate data.
- Physical access to the drive is controlled.
- Applications access only permitted files.
- Encryption keys remain protected.

---

## Common Risks

- Theft of the device
- Data recovery from discarded drives
- Unencrypted sensitive information
- Malicious USB storage devices
- Credential theft
- Data corruption
- Filesystem vulnerabilities
- Sensitive information stored in plaintext
- Backup exposure

---

## Defensive Controls

- Full-disk encryption
- Proper filesystem permissions
- Secure backups
- Drive sanitization before disposal
- Physical security
- Principle of least privilege
- Encryption of sensitive data
- Regular backups

---

## Likelihood & Impact

### Likelihood

Very High.

Every computer relies on some form of persistent storage.

### Impact

Very High.

Storage often contains the assets an attacker ultimately wants:

- Personal data
- Financial information
- Credentials
- Private documents
- Authentication tokens
- Sensitive system information

Compromise of storage can result in long-term exposure even if the system itself is later secured.

---

## Notes & Edge Cases

- Storage devices are often the attacker's objective rather than the initial entry point.
- Physical possession of a drive can bypass many operating system defenses if encryption is not used.
- Deleting a file does not necessarily remove it from the storage medium.
- Backups should generally be considered part of the storage attack surface.
- Encryption significantly changes the threat model for stolen or lost devices.

# Personal Hardening Notes Summary

Personal Device Setup
- Full Disk Encryption (LUKS).
- Strong login password.
- Separate user account from administrator privileges.
- Sensitive files stored on encrypted storage where possible.
- Regular backups.
- Verify backup restoration process periodically.
- Securely wipe drives before disposal or reuse.
- Auto-mounting of untrusted removable media reviewed.
- Only connect trusted USB storage devices.

Personal Network Setup
- N/A