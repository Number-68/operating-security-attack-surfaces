# Password Managers

## What Is It?

A password manager is an application designed to securely store, organize, and manage credentials such as passwords, passkeys, recovery codes, API keys, and other secrets.

Rather than remembering dozens or hundreds of passwords, users only need to remember a single master password (or another authentication method) to access the vault.

Common examples include Bitwarden, KeePassXC, 1Password, and Proton Pass.

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

- Users
- Authentication systems
- Browsers
- Applications
- Websites
- Multi-factor authentication systems
- Cloud synchronization services
- Encryption systems
- Operating system credential stores

---

## Why Does It Exist?

Password managers exist to help users maintain strong, unique credentials across multiple services.

They help:

- Eliminate password reuse
- Generate strong passwords
- Store credentials securely
- Reduce reliance on memory
- Simplify account management
- Improve overall authentication security

Without a password manager, many users tend to reuse passwords across multiple services, increasing risk when one account is compromised.

---

## Attack Surface

### How can an attacker interact with it?

Attackers typically target password managers indirectly through:

- Credential theft
- Malware
- Phishing attacks
- Browser compromise
- Vault theft
- Device compromise
- Social engineering

### What does it expose?

Password managers may contain:

- Passwords
- Passkeys
- Recovery codes
- API keys
- Secure notes
- Authentication secrets
- Identity information

### What trust assumptions does it make?

- The master password remains secret.
- The device running the password manager is trustworthy.
- The vault encryption functions correctly.
- Users verify websites before autofilling credentials.
- Authentication methods are properly secured.

---

## Common Risks

- Weak master passwords
- Device compromise
- Malware
- Unauthorized vault access
- Credential autofill on malicious websites
- Phishing attacks
- Improper vault backups
- Account recovery weaknesses
- Cloud account compromise

---

## Defensive Controls

- Use a strong unique master password.
- Enable multi-factor authentication.
- Secure recovery methods and recovery codes.
- Keep password manager software updated.
- Verify websites before autofilling credentials.
- Secure devices that access the vault.
- Back up vaults appropriately.
- Review stored credentials periodically.

---

## Likelihood & Impact

### Likelihood

High.

Password managers often become attractive targets because they centralize access to numerous accounts and authentication mechanisms.

However, many attacks target the user or their device rather than the password manager itself.

### Impact

Very High.

A compromised password manager may expose credentials for multiple services, accounts, and systems simultaneously.

Because password managers often sit at the center of a user's authentication ecosystem, compromise can have widespread consequences.

---

## Notes & Edge Cases

- Password managers are both a security tool and a high-value target.
- Centralizing credentials creates a concentration of risk, but for most users the security benefits significantly outweigh the risks.
- Password reuse is generally a greater risk than using a reputable password manager.
- Password managers reduce the need for memorized passwords but increase the importance of protecting the master credential.
- A password manager cannot protect against every phishing attack, especially if users are convinced to voluntarily provide credentials.
- Many modern password managers support passkeys, hardware security keys, and multi-factor authentication in addition to traditional passwords.
- For most users, a password manager is one of the highest-impact security improvements available.

# Personal Hardening Notes Summary

Personal Device Setup
- Use a strong unique master password.
- Enable multi-factor authentication.
- Store recovery codes securely.
- Keep password manager software updated.
- Use generated passwords whenever possible.
- Review stored credentials periodically.
- Secure devices that have access to the vault.

Personal Network Setup
- Use trusted networks when accessing sensitive accounts.
- Verify websites before autofilling credentials.
- Prefer encrypted connections (HTTPS).