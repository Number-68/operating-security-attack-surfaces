# operating-security-attack-surfaces
Guide to understanding the attack surfaces of the general operating system. Primarily rooted in Linux; will reference other systems for comparison.
# Overview

A lot of cybersecurity information is incredibly precise and difficult to consume. At least for me, it's hard to learn security without a tangible thing I'm trying to protect.

This repository is my attempt to understand operating system security through attack surfaces and interfaces.

I started building this while putting together my own Arch Linux security stack. For a long time, I'd install an antivirus, keep things updated, and call it a day. As I've learned more about how operating systems actually work, I've found it more useful to think about security in terms of *how* a system can be attacked rather than *what* security software I should install.

The idea I keep coming back to is:

> You can't defend what you haven't named.

If I can identify the interfaces that exist on a system, I can start learning how they work, how they can be abused, and what can be done to defend them. Kind of like finding the doors, windows, cracks, and bridges that someone might use to get inside a fortress.

This repository is essentially my personal encyclopedia and learning map for operating system security. It's a collection of attack surfaces, defenses, notes, and edge cases that help me build a better mental model of how systems are attacked and secured.

It's not meant to be a definitive guide. It's meant to help me understand my own systems better. If it helps someone else do the same, that's a bonus.

# Organization

I plan to keep most of the information in short, easily accessible files that follow a taxonomy-like structure.

```text
README.md
Image Map
Computer
├── Physical World
│   ├── Physical Access
│   ├── USB Devices
│   └── Hardware Interfaces
│
├── Hardware
│   ├── Ethernet NIC 
│   ├── Wi‑Fi NIC
│   ├── Bluetooth Adapter
│   ├── Storage Devices
│   ├── USB Controller (IN PROGRESS)
│   ├── Webcam (IN PROGRESS)
│   ├── Microphone (IN PROGRESS)
│   ├── GPU (IN PROGRESS)
│   └── TPM (IN PROGRESS)
│
├── Firmware
│   ├── BIOS (IN PROGRESS)
│   ├── UEFI (IN PROGRESS)
│   └── Device Firmware (IN PROGRESS)
│
├── Operating System
│   ├── Users (IN PROGRESS)
│   ├── Groups (IN PROGRESS)
│   ├── Permissions (IN PROGRESS)
│   ├── Services (IN PROGRESS)
│   ├── Processes (IN PROGRESS)
│   ├── Sandboxing (IN PROGRESS)
│   ├── Authentication (IN PROGRESS)
│   └── Authorization (IN PROGRESS)
│
├── Networking
│   ├── TCP/IP (IN PROGRESS)
│   ├── DNS (IN PROGRESS) 
│   ├── DHCP (IN PROGRESS)
│   ├── SSH (IN PROGRESS)
│   └── Firewalls (IN PROGRESS)
│
└── Applications
    ├── Browser (IN PROGRESS)
    ├── Password Managers (IN PROGRESS)
    ├── Containers (IN PROGRESS)
    └── Installed Software (IN PROGRESS)
```
## Entry Structure

Most entries in this repository follow a common template.

The goal is not to document every possible detail, but to quickly answer the questions that help me understand an interface, how it fits into a system, how it might be attacked, and what can be done to defend it.

```text
# Title

## What Is It?

## Where Does It Sit?
- Physical World
- Hardware
- Firmware
- Kernel
- Userspace
- Network
- Cloud / External Systems

## What Does It Interact With?

## Why Does It Exist?

## Attack Surface
How can an attacker interact with it?

What does it expose?

What trust assumptions does it make?

## Common Risks

## Defensive Controls

## Likelihood & Impact

## Notes & Edge Cases

# Personal Hardening Notes Summary
```

# Notes & Contributions

This repository is not meant to be an exhaustive catalog of every vulnerability, exploit, or edge case.

One thing I've learned from spending way too much time researching security is that you can spend forever chasing every possible vulnerability and still never catch them all. At some point, trying to defend against everything starts making your system harder for *you* to use.

The goal of this repository is awareness, not perfection.

It's meant to be an attack-surface encyclopedia that helps me understand what exists, how things can be attacked, and what kinds of defenses are available. It will continue to grow as I learn more.

A few ideas I try to keep in mind:

- You don't know what you don't know.
- Edge cases always exist.
- Assume that some layer will eventually fail.
- Have backup layers ready when it does.
- Security is often about delaying, detecting, and limiting damage rather than preventing every possible attack.

I've always thought of cybersecurity a bit like tower defense. Rather than pentesting, I often try to protect the vault.

The front line might fail. An attacker might find a vulnerability, discover a misconfiguration, or get access through some weird edge case. The goal is to have additional layers behind it that slow them down or limit what they can access, so that you can take the time to stop them entirely with your human touch.

It's a corny analogy, but it helps me think about security.

Finally, I am still learning.

If something is incorrect, incomplete, outdated, or missing important context, feel free to open an issue or contribute. The entire point of this repository is learning; you don't know what you don't know.
