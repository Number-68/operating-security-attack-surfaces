# Wi‑Fi NIC

## What Is It?

A Wi‑Fi Network Interface Controller (NIC) is a hardware component that allows a computer to communicate with wireless networks using IEEE 802.11 standards.

Instead of using a physical Ethernet cable, a Wi‑Fi NIC uses radio signals to communicate with wireless access points and other nearby devices.

---

## Where Does It Sit?

- ✅ Hardware
- ✅ Firmware
- ✅ Kernel
- ✅ Network
- ❌ Userspace
- ✅ Physical World
- ❌ Cloud / External Systems

---

## What Does It Interact With?

- Wireless access points
- Routers
- Nearby wireless devices
- Operating system networking stack
- Wireless drivers
- Wireless authentication systems (WPA/WPA2/WPA3)
- Internet-connected systems

---

## Why Does It Exist?

A Wi‑Fi NIC exists to provide network connectivity without requiring a physical cable.

It allows devices to:

- Join wireless local networks
- Access the internet
- Communicate with other devices
- Move between locations while remaining connected
- Access network resources remotely within wireless range

---

## Attack Surface

### How can an attacker interact with it?

Unlike Ethernet, a Wi‑Fi NIC broadcasts and receives radio signals through the air. This means attackers do not necessarily need physical access to a cable or network port to interact with it.

Potential interaction points include:

- Wireless frames
- Access point discovery
- Authentication processes
- Network traffic
- Device probing and scanning
- Wireless management frames

### What does it expose?

- Wireless connectivity
- Network presence
- Device identification information (MAC address)
- Wireless authentication processes
- Communication with nearby devices and access points

### What trust assumptions does it make?

- The access point being connected to is legitimate.
- Nearby devices follow networking protocols correctly.
- Authentication mechanisms are functioning properly.
- Wireless traffic is not being modified or intercepted by an attacker.

---

## Common Risks

- Rogue access points
- Evil twin attacks
- Deauthentication attacks
- Weak or compromised Wi‑Fi passwords
- Misconfigured wireless networks
- Driver vulnerabilities
- MAC address tracking
- Untrusted public Wi‑Fi networks
- Misconfigured encryption settings

---

## Defensive Controls

- Use WPA3 when available
- Use strong wireless passwords
- Keep drivers and firmware updated
- Disable Wi‑Fi when not needed
- Avoid connecting to untrusted networks
- Verify network names before connecting
- Use VPNs on untrusted networks
- Enable network firewalls
- Use randomized MAC addresses when supported

---

## Likelihood & Impact

### Likelihood

Very High.

Most modern laptops, phones, tablets, and many desktops rely on Wi‑Fi as their primary method of network access.

### Impact

High.

A compromised wireless connection can expose sensitive communications, allow access to local network resources, or provide an entry point into a system depending on the circumstances.

The most common risks usually stem from network trust decisions, weak configurations, or user behavior rather than attacks against the Wi‑Fi hardware itself.

---

## Notes & Edge Cases

- Wi‑Fi is often more exposed than Ethernet because its attack surface extends beyond physical cables and into the surrounding radio environment.
- An attacker may be able to interact with a Wi‑Fi interface without ever touching the target system physically.
- Public Wi‑Fi networks introduce additional trust concerns because network infrastructure is controlled by third parties.
- The Wi‑Fi NIC itself is rarely the ultimate target. More commonly, it serves as the pathway through which attackers interact with authentication mechanisms, network traffic, and exposed services.
- Modern Wi‑Fi security is heavily dependent on proper configuration, firmware updates, and strong authentication practices.

# Personal Hardening Notes Summary 

Personal Device Setup
- nftables configured.
- Auto-connect only for trusted networks.
- MAC randomization enabled.
- Keep system updated.
- Disable Wi‑Fi when unused.

Personal Network Setup
- WPA3 enabled.
- Strong Wi‑Fi password.
- Updated router firmware.
- Guest network for untrusted devices.