# Browser

## What Is It?

A browser is an application used to access, retrieve, and interact with content on the web.

Modern browsers do far more than display websites. They execute code, render multimedia content, store credentials, manage sessions, interact with hardware, and serve as a platform for web applications.

Common examples include Firefox, Chromium, Brave, Edge, and Safari.

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

- Websites
- Web applications
- DNS
- Network interfaces
- Authentication systems
- Password managers
- Local files
- Cookies
- Browser extensions
- Operating system APIs
- Users

---

## Why Does It Exist?

Browsers exist to provide access to web-based resources and services.

They allow users to:

- Browse websites
- Use web applications
- Download files
- Stream media
- Communicate online
- Authenticate to services
- Access cloud platforms

For many users, the browser has effectively become the primary interface to the internet.

---

## Attack Surface

### How can an attacker interact with it?

Attackers interact with browsers through web content.

Potential interaction points include:

- Malicious websites
- Phishing pages
- Malicious advertisements
- Downloads
- Browser extensions
- Scripts
- Browser vulnerabilities
- Compromised web services

### What does it expose?

Browsers may expose:

- Authentication sessions
- Stored credentials
- Cookies
- Browsing history
- Downloads
- Device information
- Browser fingerprints
- Saved form data
- User behavior

### What trust assumptions does it make?

- Websites behave legitimately.
- Downloaded files are safe.
- Browser extensions are trustworthy.
- Certificates correctly identify websites.
- Users can distinguish legitimate sites from malicious ones.

---

## Common Risks

- Phishing attacks
- Malicious downloads
- Credential theft
- Session hijacking
- Malicious browser extensions
- Tracking and fingerprinting
- Drive-by downloads
- Browser vulnerabilities
- Cross-site scripting (XSS)
- Social engineering

---

## Defensive Controls

- Keep the browser updated.
- Install extensions sparingly.
- Remove unused extensions.
- Verify URLs before entering credentials.
- Use a password manager.
- Enable multi-factor authentication where possible.
- Restrict browser permissions when appropriate.
- Download software only from trusted sources.
- Use browser sandboxing features.

---

## Likelihood & Impact

### Likelihood

Very High.

For most users, the browser is one of the most frequently used applications on the system and one of the most common ways attackers interact with users.

### Impact

High.

A compromised browser session may lead to credential theft, account compromise, malware infection, privacy violations, or access to sensitive information.

Because browsers often handle authentication and access to numerous services, they can become a high-value target.

---

## Notes & Edge Cases

- Many modern attacks target the user through the browser rather than directly attacking the operating system.
- A browser may be fully patched and still be used to compromise a user through phishing or social engineering.
- Browser extensions often receive extensive permissions and should be treated as additional attack surfaces.
- HTTPS helps authenticate the connection to a website, but it does not guarantee that the website itself is trustworthy.
- Browsers rely heavily on sandboxing because they constantly process untrusted content from the internet.
- For many users, the browser is effectively the largest attack surface on their system.

# Personal Hardening Notes Summary

Personal Device Setup
- Keep browser updated.
- Keep extensions to a minimum.
- Remove unused extensions.
- Use a password manager.
- Enable multi-factor authentication where available.
- Download files only from trusted sources.
- Review site permissions periodically.
- Consider using sandboxed browser environments when practical.

Personal Network Setup
- Use trusted DNS servers.
- Use HTTPS whenever possible.
- Avoid untrusted networks when handling sensitive accounts.

The browser is where your computer intentionally interacts with untrusted content every day; we should sandbox this and other similarly typed applications.