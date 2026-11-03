# Ethernet NIC

## What Is It?

An Ethernet Network Interface Controller (NIC) is a hardware component that allows a computer to communicate with other devices over a wired network.

It serves as the physical and logical connection between a machine and a local network through an Ethernet cable.

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

- Ethernet cables
- Network switches
- Routers
- Other devices on the local network
- The operating system's networking stack
- Network drivers
- Internet-connected systems

---

## Why Does It Exist?

Without an Ethernet NIC, a computer would not be able to communicate over a wired network.

It exists to allow devices to:

- Join local area networks (LANs)
- Access the internet
- Transfer data between systems
- Communicate with services and servers
- Receive and send network traffic

---

## Attack Surface

### How can an attacker interact with it?

An attacker generally interacts with the Ethernet NIC through network traffic rather than the hardware itself.

Potential interaction points include:

- Network packets
- Open ports
- Running network services
- Broadcast traffic
- Neighboring devices on the same network

### What does it expose?

- Network connectivity
- Reachability from other systems
- Listening services
- Device identification information (MAC address)
- Local network presence

### What trust assumptions does it make?

- The connected network is behaving correctly.
- Other devices follow networking protocols properly.
- Network infrastructure (switches, routers, DHCP servers) is trustworthy.
- Traffic reaching the machine is not necessarily malicious.

---

## Common Risks

- Network scanning and reconnaissance
- Exploitation of exposed services
- Misconfigured firewalls
- ARP spoofing
- Man-in-the-middle attacks
- DHCP attacks
- Rogue devices on local networks
- Vulnerable network drivers
- Physical access to network infrastructure

---

## Defensive Controls

- Host firewalls
- Network segmentation
- Strong authentication
- Service hardening
- Driver and system updates
- Intrusion detection and monitoring
- Physical security for network infrastructure
- Disabling unnecessary services

---

## Likelihood & Impact

### Likelihood

High.

Network interfaces are one of the most common ways systems communicate with the outside world, making them a common area for reconnaissance and attack.

### Impact

High.

Compromise of services exposed through a network interface can lead to data loss, unauthorized access, remote code execution, or lateral movement through a network.

The Ethernet NIC itself is rarely the ultimate target. It is often the path attackers use to reach the services behind it.

---

## Notes & Edge Cases

- Ethernet is often viewed as safer than Wi-Fi because physical access to the network is typically required. However, a wired connection should not automatically be considered trustworthy.
- Most attacks involving Ethernet target software, services, protocols, or trust relationships rather than the NIC hardware itself.
- In enterprise environments, the local network itself may be one of the largest attack surfaces available to an attacker.
- The Ethernet NIC is a good example of the distinction between a component and an attack surface. The NIC is the component; the network connectivity it provides is the attack surface.

# Personal Hardening Notes Summary 
Personal Device Setup:
- Firewall configured.
- Unnecessary network-facing applications not installed.
- Only required ports opened.
- System and firmware kept updated.
- Wi-Fi disabled when not needed.
- NetworkManager configured to avoid automatically joining unknown networks.


Personal Network Setup: 
- Router administration password changed from default.
- Router firmware kept updated.
- Guest network for untrusted devices.
- Separate IoT devices from primary devices.