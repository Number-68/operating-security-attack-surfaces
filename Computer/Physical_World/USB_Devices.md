# USB Devices

## What Is It?

A USB device is any peripheral that connects to a computer through the Universal Serial Bus (USB) interface.

Common examples include:

- Flash drives
- External storage devices
- Keyboards
- Mice
- Webcams
- Microphones
- Smartphones
- Security keys
- Printers
- USB network adapters

USB devices extend the functionality of a computer by providing additional capabilities through a standardized connection.

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

- USB controllers
- Users
- Device drivers
- Operating systems
- Applications
- Storage devices
- Input devices
- Authentication devices
- Peripheral hardware

---

## Why Does It Exist?

USB devices exist to provide a standardized way to connect external hardware to a computer.

They allow systems to:

- Receive user input
- Store and transfer data
- Communicate with peripherals
- Extend system functionality
- Authenticate users
- Connect specialized hardware

Without USB devices, many common workflows would require dedicated proprietary interfaces.

---

## Attack Surface

### How can an attacker interact with it?

Attackers can interact with a system by introducing a malicious or untrusted USB device.

Potential interaction points include:

- USB storage devices
- Human Interface Devices (HID)
- Smartphones
- USB hubs
- Network adapters
- Firmware-modified peripherals

### What does it expose?

USB devices may expose:

- Data transfer capabilities
- User input functionality
- Device drivers
- Filesystems
- Authentication mechanisms
- Network connectivity

### What trust assumptions does it make?

- Connected devices are legitimate.
- Devices behave as declared.
- Device firmware has not been modified.
- Users intended to connect the device.
- Drivers safely handle device behavior.

---

## Common Risks

- Malicious USB devices
- BadUSB attacks
- Keystroke injection attacks
- Infected storage devices
- Unauthorized data transfer
- Firmware tampering
- Driver vulnerabilities
- Physical access attacks
- USB devices disguising themselves as other device types

---

## Defensive Controls

- Connect only trusted USB devices.
- Avoid unknown flash drives and peripherals.
- Restrict physical access to systems.
- Keep the operating system updated.
- Keep device firmware updated where possible.
- Disable unused USB functionality when practical.
- Review newly connected devices before trusting them.
- Use encryption for sensitive removable storage.

---

## Likelihood & Impact

### Likelihood

High.

USB devices are among the most common peripherals used with computers and are frequently connected and disconnected throughout normal use.

### Impact

High.

A malicious USB device may introduce malware, emulate trusted hardware, inject user input, access sensitive data, or establish unexpected trust relationships with the operating system.

Because USB devices are often physically connected by users themselves, they can bypass many assumptions that primarily focus on network-based threats.

---

## Notes & Edge Cases

- Not all USB devices are storage devices.
- A USB device may identify itself as a keyboard, mouse, network adapter, audio device, storage device, or multiple device types simultaneously.
- Some attacks require no software vulnerability and instead rely on abusing trust placed in connected devices.
- USB devices highlight the overlap between physical security and digital security.
- A trusted-looking USB device is not necessarily a trustworthy USB device.
- Many operating systems automatically trust and initialize USB devices to improve usability, which creates opportunities for abuse.
- USB devices are best viewed as external systems requesting access to your machine through a physical interface.

# Personal Hardening Notes Summary

Personal Device Setup
- Only connect trusted USB devices.
- Avoid unknown flash drives and peripherals.
- Keep system and drivers updated.
- Lock devices when unattended.
- Use Full Disk Encryption.
- Review newly connected devices before interacting with them.

Personal Network Setup
- N/A