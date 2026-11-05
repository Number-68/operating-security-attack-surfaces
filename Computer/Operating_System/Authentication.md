# Authentication

## What Is It?

Authentication is the process of verifying the identity of a user, process, device, or service.

Before a system grants access, it must first determine whether the entity requesting access is actually who it claims to be.

Authentication answers the question:

"Who are you?"

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

- Users
- Groups
- Permissions
- Authorization systems
- Login interfaces
- Password managers
- Multi-factor authentication systems
- Services
- Applications
- Network resources

---

## Why Does It Exist?

Authentication exists to establish identity before access is granted.

It helps systems:

- Verify users
- Restrict unauthorized access
- Protect sensitive data
- Establish accountability
- Enforce security policies

Without authentication, systems would have no reliable way of determining who is requesting access.

---

## Attack Surface

### How can an attacker interact with it?

Authentication mechanisms are frequently targeted because they protect access to users, systems, and data.

Potential interaction points include:

- Login forms
- Password prompts
- Authentication tokens
- Session cookies
- SSH keys
- Password databases
- Multi-factor authentication systems

### What does it expose?

Authentication mechanisms may expose:

- Login interfaces
- User identities
- Authentication secrets
- Session information
- Access workflows

### What trust assumptions does it make?

- Users protect their credentials.
- Authentication mechanisms function correctly.
- Passwords remain secret.
- Authentication tokens are protected.
- Successful authentication corresponds to a legitimate identity.

---

## Common Risks

- Weak passwords
- Password reuse
- Credential theft
- Phishing attacks
- Social engineering
- Brute-force attacks
- Credential stuffing
- Session hijacking
- Stolen authentication tokens
- Misconfigured authentication systems

---

## Defensive Controls

- Use strong unique passwords.
- Utilize a password manager.
- Enable multi-factor authentication.
- Protect authentication tokens.
- Limit login attempts where appropriate.
- Monitor authentication activity.
- Use secure authentication protocols.
- Remove unused accounts.

---

## Likelihood & Impact

### Likelihood

Very High.

Authentication systems are one of the most frequently targeted security mechanisms because they protect access to users, data, and resources.

Most attackers would rather steal valid credentials than exploit complex technical vulnerabilities.

### Impact

High.

Successful authentication bypass or credential compromise often grants an attacker legitimate access to resources.

The impact depends on the privileges associated with the compromised identity.

---

## Notes & Edge Cases

- Authentication does not determine what actions are allowed. It only verifies identity.
- Authentication and authorization are often confused but serve different purposes.
- Authentication can be based on:
  - Something you know (password)
  - Something you have (security key)
  - Something you are (biometrics)
- Multi-factor authentication combines multiple forms of authentication.
- A strong authentication system cannot fully protect against a compromised account holder.
- Many attacks target users directly because obtaining valid credentials is often easier than exploiting technical vulnerabilities.

# Personal Hardening Notes Summary

Personal Device Setup
- Use strong unique passwords.
- Use a password manager.
- Enable multi-factor authentication where available.
- Protect recovery codes and backup methods.
- Remove unused accounts.
- Review authentication settings periodically.

Personal Network Setup
- Restrict remote authentication services when unnecessary.
- Use SSH keys instead of passwords where practical.