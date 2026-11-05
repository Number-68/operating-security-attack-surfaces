# Processes

## What Is It?

A process is an actively running instance of a program.

Whenever an application, service, script, or system component executes, the operating system creates one or more processes to perform that work.

Processes are the primary way software executes and interacts with system resources.

---

## Where Does It Sit?

- ❌ Physical World
- ❌ Hardware
- ❌ Firmware
- ✅ Kernel
- ✅ Userspace
- ❌ Network
- ❌ Cloud / External Systems

---

## What Does It Interact With?

- Users
- Groups
- Permissions
- Services
- Files and directories
- Memory
- CPU
- Hardware devices
- Other processes
- Operating system resources

---

## Why Does It Exist?

Processes exist to execute code and perform work on behalf of users, applications, and the operating system.

They allow a system to:

- Run applications
- Perform background tasks
- Manage services
- Execute scripts
- Access system resources
- Perform computations

Without processes, software would not be able to run.

---

## Attack Surface

### How can an attacker interact with it?

Attackers often interact with processes after gaining access to a system or by exploiting vulnerable software.

Potential interaction points include:

- Vulnerable applications
- Running services
- Process communication mechanisms
- Shared resources
- Memory corruption vulnerabilities
- Privilege escalation opportunities

### What does it expose?

Processes may expose:

- Running code
- Allocated memory
- Open files
- Network connections
- System resources
- Inter-process communication channels

### What trust assumptions does it make?

- Processes only access resources they are permitted to use.
- Process isolation functions correctly.
- Applications behave as intended.
- Users only execute trusted software.
- The operating system correctly enforces security boundaries.

---

## Common Risks

- Malware execution
- Vulnerable applications
- Privilege escalation
- Code injection
- Process hijacking
- Memory corruption vulnerabilities
- Excessive process privileges
- Untrusted code execution
- Information leakage between processes

---

## Defensive Controls

- Apply the principle of least privilege.
- Keep software updated.
- Remove unnecessary applications.
- Use process isolation mechanisms.
- Utilize sandboxing where appropriate.
- Monitor running processes.
- Verify software sources before execution.
- Restrict unnecessary administrative privileges.

---

## Likelihood & Impact

### Likelihood

Very High.

Every running application, service, and background task exists as one or more processes.

Most attacks ultimately target a process because processes are responsible for executing code and interacting with system resources.

### Impact

High.

A compromised process can potentially access data, communicate over the network, interact with other resources, or attempt to escalate privileges.

The impact depends heavily on the permissions and privileges assigned to the process.

---

## Notes & Edge Cases

- A service is not the same thing as a process, though services often run as one or more processes.
- Multiple processes may originate from the same application.
- Modern operating systems rely heavily on process isolation to maintain security.
- Most software vulnerabilities eventually affect a process that is executing vulnerable code.
- Many security boundaries within an operating system are ultimately enforced between processes.
- Processes answer the question: "What is executing right now?"

# Personal Hardening Notes Summary

Personal Device Setup
- Keep software updated.
- Run only trusted applications.
- Remove unused software.
- Review running processes periodically.
- Avoid running applications with unnecessary privileges.
- Use sandboxing for untrusted applications when practical.

Personal Network Setup
- N/A

Takeaway, run proceses that are trusted, and sandbox processes(applications) that are untrust worthy. 
Maybe also browsers too since they are the portal to the web and could possibly harbor some unwanted... things.