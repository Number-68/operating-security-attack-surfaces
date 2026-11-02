# operating-security-attack-surfaces
Guide to understanding the attack surfaces of the general operating system. Primarily rooted in Linux; will reference other systems for comparison.
# Thesis

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
├── Network
├── Firmware
├── Runtime
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