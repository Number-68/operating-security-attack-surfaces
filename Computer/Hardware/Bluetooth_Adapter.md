# Bluetooth Adapter

## What Is It?

A Bluetooth adapter is a hardware component that allows a computer to communicate wirelessly with nearby devices over short distances.

It is commonly used for connecting peripherals such as keyboards, mice, headphones, speakers, game controllers, phones, and other Bluetooth-enabled devices.

Unlike Wi‑Fi, Bluetooth is generally designed for direct device-to-device communication rather than connecting to local networks or the internet.

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

- Wireless peripherals
- Phones and tablets
- Headphones and speakers
- Keyboards and mice
- Game controllers
- Operating system Bluetooth services
- Bluetooth drivers
- Nearby Bluetooth-enabled devices

---

## Why Does It Exist?

Bluetooth exists to allow convenient wireless communication between nearby devices.

Without Bluetooth, users would need cables or alternative wireless technologies for many common peripherals and device-to-device interactions.

Common uses include:

- Wireless audio
- Wireless peripherals
- File transfers
- Device synchronization
- Device discovery and pairing
- Communication with smart devices

---

## Attack Surface

### How can an attacker interact with it?

An attacker can interact with a Bluetooth adapter if they are within wireless range and the adapter is enabled.

Potential interaction points include:

- Device discovery
- Pairing requests
- Bluetooth profiles and services
- Wireless radio communications
- Vulnerable Bluetooth implementations
- Connected devices

### What does it expose?

- Bluetooth device discovery
- Pairing mechanisms
- Device identifiers
- Wireless communication channels
- Services provided over Bluetooth

### What trust assumptions does it make?

- Nearby devices are legitimate.
- Pairing requests are authorized by the user.
- Connected devices behave as expected.
- Bluetooth implementations correctly enforce security controls.

---

## Common Risks

- Unauthorized pairing attempts
- Device impersonation
- Information disclosure
- Device tracking through identifiers
- Vulnerable Bluetooth services
- Weak pairing configurations
- Firmware vulnerabilities
- Malicious or compromised peripherals
- Excessive Bluetooth permissions

---

## Defensive Controls

- Disable Bluetooth when not needed.
- Remove unused or forgotten pairings.
- Keep system, drivers, and firmware updated.
- Only pair with trusted devices.
- Review Bluetooth permissions and settings.
- Disable device discoverability when not actively pairing.
- Use modern Bluetooth standards and security features when available.

---

## Likelihood & Impact

### Likelihood

Moderate.

Bluetooth is widely available on modern laptops, phones, and desktop systems. However, many users keep it disabled or only use it occasionally.

### Impact

Low to Moderate.

Most Bluetooth attacks require physical proximity to the target device. While Bluetooth has experienced notable vulnerabilities over the years, it generally represents a smaller attack surface than internet-facing network interfaces.

The impact depends heavily on what devices are connected, what services are exposed, and whether the adapter is actively being used.

---

## Notes & Edge Cases

- Bluetooth is frequently overlooked because many people view it as a convenience feature rather than a communication interface.
- Unlike Ethernet and Wi‑Fi, Bluetooth attacks usually require an attacker to be physically nearby.
- Bluetooth creates trust relationships with external devices. A compromised peripheral may introduce risks that originate outside the computer itself.
- Modern operating systems generally place significant restrictions around Bluetooth interactions, but vulnerabilities still occur in drivers, firmware, and protocol implementations.
- Bluetooth is a good example of an attack surface that may be inactive most of the time but can become relevant the moment pairing or device discovery is enabled.

# Personal Hardening Notes summary
Personal Device Setup:
- Bluetooth disabled when not actively in use.
- Device discoverability disabled except during pairing.
- Remove unused paired devices periodically.
- Keep system and firmware updated.
- Only pair trusted devices.
- Review paired devices occasionally.

Personal Network Setup:
- N/A

Bluetooth by itself seems to be pretty hardened; it's pretty low maintenance. Not much third party hardening is needed; just practice standard practices and this interface won't give too much headaches.