# DNS (Domain Name System)

## What Is It?

DNS (Domain Name System) is a protocol and distributed system responsible for translating human-readable domain names into IP addresses.

It allows users to access websites and services using names such as:

- google.com
- microsoft.com
- github.com

instead of needing to remember numerical IP addresses.

DNS is often described as the internet's phone book.

---

## Where Does It Sit?

- ❌ Physical World
- ❌ Hardware
- ❌ Firmware
- ❌ Kernel
- ✅ Userspace
- ✅ Network
- ✅ Cloud / External Systems

---

## What Does It Interact With?

- Web browsers
- Applications
- Operating systems
- Network interfaces
- Routers
- DNS servers
- ISPs
- Public DNS providers
- Remote internet services

---

## Why Does It Exist?

DNS exists to make networking usable.

Instead of requiring users to remember numerical IP addresses, DNS allows systems to locate resources through human-readable names.

DNS helps:

- Locate websites
- Discover internet services
- Simplify network communication
- Route traffic to intended destinations

Without DNS, most internet services would be significantly harder to use.

---

## Attack Surface

### How can an attacker interact with it?

Attackers can interact with DNS by influencing or manipulating the DNS information a device receives.

Potential interaction points include:

- Rogue DNS servers
- DNS poisoning
- DNS hijacking
- Malicious network configurations
- Misconfigured routers
- Compromised DNS providers

### What does it expose?

DNS exposes:

- Domain lookup requests
- Destination information
- Website and service discovery
- Network communication patterns

### What trust assumptions does it make?

- DNS servers return accurate information.
- DNS responses have not been tampered with.
- Configured DNS providers are trustworthy.
- Networks are providing legitimate DNS settings.
- Resolved destinations match their intended services.

---

## Common Risks

- DNS poisoning
- DNS hijacking
- Malicious DNS servers
- Traffic redirection
- Phishing through manipulated DNS responses
- Privacy leakage
- DNS misconfiguration
- Compromised DNS providers
- Network-level attacks

---

## Defensive Controls

- Use trusted DNS providers.
- Validate DNS settings periodically.
- Consider DNSSEC-aware resolvers when available.
- Use encrypted DNS technologies when appropriate.
- Secure routers and networking equipment.
- Verify suspicious redirects or certificate warnings.
- Monitor for unexpected DNS changes.

---

## Likelihood & Impact

### Likelihood

High.

Every internet-connected device relies on DNS regularly. Most users interact with DNS dozens or hundreds of times per day without realizing it.

### Impact

High.

Compromised DNS can redirect users to malicious destinations, intercept communications, facilitate phishing attacks, or alter how systems interact with network resources.

Because DNS sits near the beginning of many network connections, compromise can affect numerous services simultaneously.

---

## Notes & Edge Cases

- DNS does not determine whether a website is trustworthy; it only helps locate it.
- DNS is commonly invisible to users because it operates automatically in the background.
- DNS is one of the most important trust relationships on a network.
- A malicious DNS response can send users somewhere they never intended to go.
- Many attacks target user trust rather than the DNS protocol itself.
- DHCP often determines which DNS server a device will use.
- DNS is a good example of a foundational internet service that most users rarely think about until something goes wrong.

# Personal Hardening Notes Summary

Personal Device Setup
- Understand which DNS servers are being used.
- Verify DNS settings when troubleshooting unusual network behavior.
- Keep networking software updated.
- Be cautious of unexpected certificate warnings or redirects.

Personal Network Setup
- Use trusted DNS providers.
- Secure router configuration.
- Review DNS settings periodically.
- Prevent unauthorized changes to network configuration.
- Consider encrypted DNS where practical.