# TCP/IP

## What Is It?

TCP/IP (Transmission Control Protocol / Internet Protocol) is the foundational networking suite that allows computers and devices to communicate with one another across local networks and the internet.

Most modern networking depends on TCP/IP. Protocols such as HTTP, HTTPS, SSH, DNS, and many others operate on top of it.

At a high level:

- IP determines where data should go.
- TCP helps ensure data arrives correctly and in order.

---

## Where Does It Sit?

- ❌ Physical World
- ❌ Hardware
- ❌ Firmware
- ✅ Kernel
- ✅ Userspace
- ✅ Network
- ✅ Cloud / External Systems

---

## What Does It Interact With?

- Ethernet NICs
- Wi‑Fi NICs
- Routers
- Switches
- Firewalls
- DNS
- DHCP
- Services
- Applications
- Remote systems

---

## Why Does It Exist?

TCP/IP exists to allow devices to communicate across networks.

It provides:

- Device addressing
- Data transmission
- Routing
- Communication reliability
- Internet connectivity
- Network interoperability

Without TCP/IP, modern networking would not function as we know it.

---

## Attack Surface

### How can an attacker interact with it?

Attackers interact with TCP/IP whenever they communicate with a system across a network.

Potential interaction points include:

- Open ports
- Network services
- Network packets
- Routing mechanisms
- Protocol implementations
- Misconfigured network services

### What does it expose?

TCP/IP exposes:

- Network connectivity
- Reachable services
- Open ports
- Device addresses
- Communication channels

### What trust assumptions does it make?

- Devices correctly identify themselves.
- Network traffic is delivered as expected.
- Remote systems are who they claim to be.
- Communication paths are trustworthy.
- Applications properly validate received data.

---

## Common Risks

- Network scanning
- Reconnaissance
- Spoofing
- Man-in-the-middle attacks
- Service exploitation
- Traffic interception
- Denial-of-service attacks
- Protocol implementation vulnerabilities
- Misconfigured network services

---

## Defensive Controls

- Use host firewalls.
- Disable unnecessary services.
- Restrict exposed ports.
- Use encryption (HTTPS, SSH, VPNs, etc.).
- Keep systems and networking software updated.
- Monitor listening services and network activity.
- Follow the principle of least privilege.

---

## Likelihood & Impact

### Likelihood

Very High.

Every network-connected device relies on TCP/IP and exposes some portion of its functionality through it.

Most network-based attacks ultimately travel through the TCP/IP stack.

### Impact

High.

Compromising services accessible through TCP/IP can lead to unauthorized access, data exposure, remote code execution, denial-of-service conditions, or further compromise of a system.

The impact depends largely on what services are exposed through the protocol suite.

---

## Notes & Edge Cases

- TCP/IP itself is not inherently insecure. It is the foundation that enables communication.
- Most people do not directly interact with TCP/IP, but nearly every network application depends on it.
- Higher-level protocols such as HTTP, HTTPS, SSH, DNS, and SMTP all rely on TCP/IP.
- TCP/IP is less of a single attack surface and more of the highway through which many attack surfaces are reached.
- Firewalls, encryption, authentication, and network segmentation often exist to help secure communication that occurs over TCP/IP.
- Understanding TCP/IP helps explain how attackers discover, reach, and interact with networked systems.

# Personal Hardening Notes Summary

Personal Device Setup
- Keep the operating system updated.
- Keep networking software updated.
- Disable unnecessary network services.
- Use a properly configured firewall.
- Review listening ports periodically.

Personal Network Setup
- Restrict unnecessary exposed services.
- Use secure protocols (HTTPS, SSH, VPNs) where appropriate.
- Maintain router and network equipment.
- Segment trusted and untrusted devices when practical.