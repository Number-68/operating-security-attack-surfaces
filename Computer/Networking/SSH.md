# SSH (Secure Shell)

## What Is It?

SSH (Secure Shell) is a secure network protocol that allows users to remotely access and manage systems over a network.

It is commonly used for:

- Remote terminal access
- Remote system administration
- Secure file transfers
- Remote command execution
- Server management

SSH encrypts communication between systems to protect data from interception and tampering.

---

## Where Does It Sit?

- ❌ Physical World
- ❌ Hardware
- ❌ Firmware
- ✅ Kernel
- ✅ Userspace
- ✅ Network
- ❌ Cloud / External Systems

---

## What Does It Interact With?

- Users
- Authentication systems
- Authorization systems
- Services
- Processes
- Network interfaces
- Firewalls
- Remote systems
- Filesystems
- SSH keys

---

## Why Does It Exist?

SSH exists to provide secure remote access to systems.

It allows administrators and users to:

- Manage systems remotely
- Execute commands remotely
- Transfer files securely
- Automate administrative tasks
- Access servers from remote locations

Without SSH, remote administration would require less secure protocols or physical access to the machine.

---

## Attack Surface

### How can an attacker interact with it?

Because SSH is designed to accept remote connections, it is directly exposed to interaction from other systems.

Potential interaction points include:

- Login attempts
- Password authentication
- SSH key authentication
- Open SSH ports
- Exposed internet-facing servers
- Misconfigured SSH settings

### What does it expose?

SSH may expose:

- Remote login functionality
- Terminal access
- File transfer capabilities
- User accounts
- Authentication mechanisms
- Administrative functionality

### What trust assumptions does it make?

- Users connecting are legitimate.
- Authentication mechanisms are secure.
- Credentials have not been compromised.
- Remote systems are trusted.
- Authorized users behave appropriately.

---

## Common Risks

- Weak passwords
- Brute-force login attempts
- Stolen SSH keys
- Credential theft
- Exposed internet-facing SSH services
- Misconfigured SSH settings
- Excessive user privileges
- Unauthorized key distribution
- Reused credentials

---

## Defensive Controls

- Use SSH keys instead of passwords.
- Disable password authentication where practical.
- Restrict which users may access SSH.
- Disable root login.
- Keep OpenSSH updated.
- Use a firewall to restrict access.
- Remove unused authorized keys.
- Review SSH configuration periodically.
- Monitor login activity and authentication attempts.

---

## Likelihood & Impact

### Likelihood

High.

SSH is one of the most commonly deployed remote administration solutions and is frequently targeted by automated scanning and login attempts when exposed to networks.

### Impact

High.

A successful compromise of SSH may provide direct access to the system as a legitimate user.

The impact depends heavily on the privileges of the compromised account.

---

## Notes & Edge Cases

- SSH is not inherently unsafe. In many environments it is one of the most secure methods of remote administration.
- The existence of SSH is not the risk. Poor configuration is usually the risk.
- A machine that does not run an SSH service generally cannot be attacked through SSH.
- SSH keys are typically stronger than password-based authentication when managed properly.
- Firewalls and SSH often work together. The firewall determines who can attempt a connection, while SSH determines who is allowed to log in.
- SSH is one of the clearest examples of an intentionally exposed attack surface. Its purpose is to allow remote access while controlling who receives that access.

# Personal Hardening Notes Summary

Personal Device Setup
Daily Driver
- SSH disabled.
- OpenSSH not enabled unless specifically needed.
Server
- Use SSH key authentication.
- Disable root login.
- Restrict SSH access to required users.
- Keep OpenSSH updated.
- Review authorized keys periodically.

Personal Network Setup
- Restrict SSH access through the firewall.
- Do not expose SSH to the internet unless necessary.
- Limit network access to trusted hosts when practical.
- Review exposed ports periodically.

Mostly just mapping and configuration and a specific type of login with a key rather than just a password.