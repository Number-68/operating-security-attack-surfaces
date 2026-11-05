# DHCP (Dynamic Host Configuration Protocol)

## What Is It?

DHCP (Dynamic Host Configuration Protocol) is a network protocol that automatically assigns network configuration information to devices when they join a network.

Instead of manually configuring every device, DHCP provides settings such as:

- IP addresses
- Subnet masks
- Default gateways
- DNS servers

Most home and business networks rely on DHCP to simplify network management.

---

## Where Does It Sit?

- ❌ Physical World
- ❌ Hardware
- ❌ Firmware
- ❌ Kernel
- ✅ Userspace
- ✅ Network
- ❌ Cloud / External Systems

---

## What Does It Interact With?

- Computers
- Phones
- Tablets
- Routers
- Switches
- Access points
- DNS servers
- Operating system network managers
- Local network devices

---

## Why Does It Exist?

DHCP exists to automate network configuration.

Without DHCP, administrators would need to manually assign network settings to every device.

DHCP helps:

- Simplify device onboarding
- Reduce configuration errors
- Manage IP address allocation
- Provide consistent network settings
- Improve network usability

---

## Attack Surface

### How can an attacker interact with it?

Attackers typically interact with DHCP from within the local network.

Potential interaction points include:

- Rogue DHCP servers
- DHCP requests
- DHCP responses
- Network joining processes
- Device provisioning

### What does it expose?

DHCP exposes network configuration information such as:

- Assigned IP addresses
- DNS server assignments
- Default gateway assignments
- Network topology information

### What trust assumptions does it make?

- The DHCP server is legitimate.
- Network configuration information provided is trustworthy.
- Devices receive configuration from the intended source.
- The local network is reasonably trusted.

---

## Common Risks

- Rogue DHCP servers
- Malicious network configuration
- DNS manipulation
- Traffic redirection
- Network reconnaissance
- Misconfigured DHCP servers
- Accidental address conflicts
- Man-in-the-middle opportunities

---

## Defensive Controls

- Restrict unauthorized devices from providing DHCP services.
- Secure network infrastructure.
- Segment trusted and untrusted devices.
- Verify DNS and gateway configurations.
- Monitor for unexpected DHCP servers.
- Use trusted network environments.
- Review assigned network settings when troubleshooting suspicious behavior.

---

## Likelihood & Impact

### Likelihood

Moderate.

Most users interact with DHCP every day without realizing it. DHCP-related attacks are less common than phishing, credential theft, or software vulnerabilities, but can occur on shared or untrusted networks.

### Impact

Moderate to High.

A malicious DHCP server may be able to influence how devices communicate on a network by providing dangerous configuration information.

The impact depends on what network settings are altered and how much trust is placed in the affected network.

---

## Notes & Edge Cases

- DHCP is usually invisible to end users because it operates automatically in the background.
- Most home routers act as DHCP servers.
- DHCP itself does not provide security. Its job is convenience and automation.
- A compromised DHCP service may redirect traffic by assigning malicious DNS servers or incorrect gateways.
- Public, shared, or untrusted networks generally present more DHCP-related risk than a typical home network.
- DHCP is a good example of a protocol that is usually safe when the surrounding network is trustworthy.

# Personal Hardening Notes Summary

Personal Device Setup
- Use known and trusted networks when possible.
- Verify unusual network settings if network behavior seems suspicious.
- Keep networking software and the operating system updated.
- Understand which DNS servers are being assigned to the system.

Personal Network Setup
- Use a trusted router as the DHCP server.
- Prevent unauthorized devices from providing DHCP services.
- Review router DHCP settings periodically.
- Use trusted DNS providers when appropriate.
- Separate trusted and untrusted devices where practical.