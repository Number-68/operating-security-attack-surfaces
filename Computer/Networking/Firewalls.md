# Firewalls

## What Is It?

A firewall is a security mechanism that monitors, filters, and controls network traffic entering or leaving a system.

Firewalls allow administrators to define rules that determine which network connections are permitted and which should be blocked.

Their primary purpose is to reduce unnecessary network exposure and limit unauthorized communication.

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

- Network interfaces
- Services
- Applications
- Processes
- Ports
- Protocols
- Routers
- Remote systems
- Operating system networking stacks

---

## Why Does It Exist?

Firewalls exist to control network communication.

They help:

- Block unwanted traffic
- Restrict access to services
- Limit exposure to attackers
- Enforce network security policies
- Reduce attack surface
- Control inbound and outbound connections

Without a firewall, services may be exposed more broadly than intended.

---

## Attack Surface

### How can an attacker interact with it?

Attackers typically interact with firewalls indirectly by attempting to communicate with services protected by firewall rules.

Common goals include:

- Finding open ports
- Discovering exposed services
- Bypassing firewall rules
- Leveraging misconfigurations
- Exploiting overly permissive configurations

### What does it expose?

Firewalls expose:

- Allowed ports
- Allowed protocols
- Permitted network services
- Defined network policies

### What trust assumptions does it make?

- Firewall rules are configured correctly.
- Allowed services are intended to be exposed.
- Administrators understand the consequences of their rules.
- Applications receiving traffic behave securely.

---

## Common Risks

- Overly permissive rules
- Unnecessary open ports
- Misconfigured firewall policies
- Forgotten exceptions
- Disabled firewalls
- Exposed administrative interfaces
- Unfiltered outbound traffic
- Incorrect trust assumptions about internal networks

---

## Defensive Controls

- Default deny where practical.
- Open only required ports.
- Review firewall rules regularly.
- Remove unnecessary exceptions.
- Restrict exposed services.
- Monitor listening ports.
- Document firewall changes.
- Segment networks when appropriate.

---

## Likelihood & Impact

### Likelihood

Very High.

Most systems connected to a network rely on some form of firewalling, whether provided by the operating system, a router, or dedicated network equipment.

Firewall misconfigurations are a common source of unintended exposure.

### Impact

High.

A properly configured firewall can significantly reduce network exposure.

A poorly configured firewall may allow attackers to access services or resources that were never intended to be publicly reachable.

---

## Notes & Edge Cases

- A firewall does not secure a vulnerable service. It only controls whether traffic can reach it.
- Firewalls reduce exposure; they do not replace secure configuration.
- Many home users rely on both a host firewall and a router firewall.
- Firewalls can control both incoming and outgoing traffic.
- If a service is not running, it generally does not need a firewall rule.
- Firewalls work best when combined with least privilege, service hardening, and proper network design.
- A common principle is: "If it does not need network access, block it."

# Personal Hardening Notes Summary
Personal Device Setup
- Use nftables as the primary firewall.
- Default deny inbound traffic.
- Allow only required ports and services.
- Review firewall rules periodically.
- Remove temporary rules when no longer needed.
- Verify firewall behavior after major system changes.

Personal Network Setup
- Use router-based firewall protections.
- Do not expose services to the internet unless necessary.
- Review port forwarding rules periodically.
- Separate trusted and untrusted devices when practical.

This is something I'll have to hash out more, but configuring your firewall doesn't mean it's completely safe. However, ensuring that you limit the attack surfaces is it's goal. You will have other deterrants after that, but this is something to keep in mind when you're configuring the firewall. You can't protect against everything, but you can get a good minimum.