# USB Controller

## What Is It?

A USB (Universal Serial Bus) Controller is a hardware component responsible for managing communication between the computer and USB-connected devices.

It acts as the bridge between the operating system and USB peripherals such as keyboards, mice, storage devices, webcams, microphones, smartphones, security keys, and countless other devices.

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

- USB keyboards
- USB mice
- USB storage devices
- USB hubs
- Smartphones
- Security keys
- External drives
- Printers
- Cameras and webcams
- Audio devices
- Operating system drivers
- Firmware

---

## Why Does It Exist?

The USB Controller exists to provide a standardized method for connecting external devices to a computer.

Without it, every peripheral would require its own connection standard and communication method.

It enables:

- Data transfer
- Peripheral connectivity
- Device charging
- Hardware expansion
- User input
- External storage access

---

## Attack Surface

### How can an attacker interact with it?

An attacker can interact with the USB Controller by introducing a device that the controller recognizes and trusts.

Because USB is designed for convenience, many devices are automatically detected and connected with little user interaction.

Potential interaction points include:

- USB storage devices
- Keyboards
- Mice
- Smartphones
- USB network adapters
- USB hubs
- Firmware-level USB devices
- Malicious peripherals

### What does it expose?

- Direct communication with attached devices
- Human Interface Device (HID) functionality
- File transfer capabilities
- Driver interactions
- Device identification mechanisms
- Peripheral trust relationships

### What trust assumptions does it make?

- Connected devices are what they claim to be.
- Devices behave according to USB standards.
- Users intentionally connected the device.
- Device firmware has not been modified maliciously.
- Drivers safely handle device behavior.

---

## Common Risks

- Malicious USB devices
- BadUSB attacks
- Keystroke injection attacks
- Rogue keyboards or mice
- Malware delivered through removable media
- Unauthorized data transfer
- Firmware manipulation
- Vulnerable USB drivers
- Physical access attacks
- USB devices masquerading as other device types

---

## Defensive Controls

- Only connect trusted USB devices.
- Disable unused USB ports where practical.
- Use screen locking when unattended.
- Restrict physical access to the machine.
- Keep system and firmware updated.
- Disable automatic execution of removable media.
- Use device control policies if available.
- Encrypt sensitive data stored on removable media.
- Monitor connected devices periodically.

---

## Likelihood & Impact

### Likelihood

High.

USB is one of the most common methods for connecting external devices to a computer. Most systems interact with USB devices daily.

### Impact

High.

USB devices can introduce new hardware, provide unauthorized input, transfer malicious files, or create unexpected trust relationships with the operating system.

A successful USB attack may bypass many network-based security controls because the device appears to be physically connected and trusted.

---

## Notes & Edge Cases

- USB is often treated as a convenience feature, but it is also a significant trust boundary.
- Not all USB devices are storage devices. A USB device may identify itself as a keyboard, mouse, network adapter, audio device, or multiple device types at once.
- A malicious USB device may never store a file and still compromise a system.
- Physical access often turns USB into one of the most powerful attack surfaces available.
- Modern operating systems include numerous protections, but many attacks rely on users assuming that all USB devices are trustworthy.
- USB demonstrates an important security principle: a device that appears harmless may expose far more functionality than expected.


# Personal Hardening Notes Summary

Personal Device Setup
- Only connect trusted USB devices.
- Screen automatically locks when unattended.
- Keep kernel, firmware, and system packages updated.
- Disable automatic mounting or review auto-mount behavior.
- Verify newly connected devices before interacting with them.
- Avoid using unknown flash drives or peripherals.
- Remove unnecessary USB devices when not in use.
- Full disk encryption enabled (helps mitigate physical access risks).

Personal Network Setup
- N/A

Final Note, figure out if there's some USB management service for your chosen device.