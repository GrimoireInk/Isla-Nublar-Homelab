# 🔐 Security Policy

## Purpose

Public documentation should demonstrate how the environment works without exposing credentials, private keys, sensitive configuration data, or information that could unnecessarily increase risk to the real environment.

---

## Lab Scope

Security testing performed as part of this project is limited to:

- Systems I own or am explicitly authorized to test
- Virtual machines and containers created for the lab
- Intentionally vulnerable applications and operating systems
- Capture-the-Flag environments
- Isolated Active Directory attack/defense labs
- Other authorized educational environments

The `PADDOCK` security zone is intended for offensive-security exercises and intentionally vulnerable systems.

Intentionally vulnerable systems should remain isolated from trusted devices and should not be exposed directly to the public Internet unless there is a specific, understood, and documented reason to do so.

---

## Repository Security Rules

The following information must **never** be intentionally committed to this repository:

- Passwords
- API keys
- Access tokens
- Session tokens or cookies
- SSH private keys
- TLS/SSL private keys
- Recovery codes
- Authentication secrets
- Cloud credentials
- VPN credentials
- Database passwords
- Real production credentials
- Unredacted backup files containing secrets
- Private certificates containing sensitive key material

Examples of files that should remain local include:

```text
.env
.env.*
*.key
*.pem
*.pfx
*.p12
credentials.*
secrets.*
*.token
terraform.tfvars
*.tfstate
```

The repository's `.gitignore` provides an additional safeguard, but **a `.gitignore` file is not a security boundary**. Files must still be reviewed before they are committed.

---

## Information That Should Be Sanitized

Before publishing configuration files, screenshots, diagrams, command output, or logs, review them for information that does not need to be public.

Examples include:

- Public IP addresses
- MAC addresses when unnecessary
- Device serial numbers
- Hardware UUIDs
- Account usernames that identify real services or people
- Internal hostnames outside the documented lab naming scheme
- Authentication headers
- Cookies
- Email addresses
- VPN configuration details
- Wireless credentials
- Router or firewall administration information
- Cloud tenant or subscription identifiers
- Personally identifiable information
- School or workplace information that is unrelated to the technical lesson

Private RFC1918 addresses such as `10.0.0.0/8`, `172.16.0.0/12`, and `192.168.0.0/16` are not credentials, but diagrams and examples may still use sanitized addresses when publishing the real layout provides no educational value.

---

## Safe Configuration Examples

Public configuration files should use placeholders when sensitive values would otherwise be required.

For example:

```text
USERNAME=<REDACTED>
PASSWORD=<REDACTED>
API_TOKEN=<REDACTED>
PUBLIC_IP=<REDACTED>
VPN_SECRET=<REDACTED>
```

Example domains, usernames, networks, and credentials should be clearly fictional.

---

## Network Isolation

Security-testing systems should be separated from trusted systems through network segmentation and firewall policy.

Planned security zones include:

| Zone | Security Purpose |
|---|---|
| **CONTROL CENTER** | Infrastructure management |
| **VISITOR CENTER** | General-purpose systems |
| **GENETICS LAB** | Development and research |
| **PADDOCK** | Isolated security-testing environment |
| **HATCHERY** | Containers and experimental services |
| **SITE B** | Backup infrastructure |

The goal is to ensure that intentionally vulnerable or compromised lab machines cannot freely reach trusted devices.

Firewall rules, VLANs, routing, and isolation controls will be documented as the network architecture develops.

---

## Vulnerable Systems

Intentionally vulnerable systems may include technologies such as:

- Metasploitable
- OWASP Juice Shop
- DVWA
- Vulnerable Windows or Linux virtual machines
- Purpose-built Active Directory attack labs
- CTF targets

These systems are expected to contain security weaknesses by design.

They should:

- Remain inside authorized lab environments
- Be isolated from trusted networks
- Avoid unnecessary Internet exposure
- Use non-production credentials
- Contain no sensitive personal information
- Be destroyed, reverted, or rebuilt when appropriate after exercises

---

## Offensive-Security Tools

This project may document legitimate cybersecurity tools used for learning, testing, and defensive research.

Examples may include:

- Kali Linux
- Nmap
- Wireshark
- Burp Suite
- Metasploit
- BloodHound
- Impacket
- Hashcat
- John the Ripper
- Security Onion
- Wazuh
- Suricata
- Zeek

Their presence in this repository does not imply authorization to use them against systems outside the lab.

All testing must remain within systems that are owned or explicitly authorized for testing.

---

## Secrets Accidentally Committed

If a real credential, key, token, or other secret is accidentally committed:

1. **Assume the secret is compromised.**
2. Revoke or rotate the exposed secret immediately.
3. Remove the secret from the current repository contents.
4. Remove the secret from Git history when appropriate.
5. Verify that no copies remain in branches, tags, logs, artifacts, or documentation.
6. Review related systems for unexpected access.
7. Document the incident in a sanitized way if it provides a useful learning opportunity.

Deleting a secret in a later commit does **not** make the original secret safe.

---

## Pre-Commit Security Checklist

Before pushing changes, verify:

- [ ] No passwords are present
- [ ] No API keys or tokens are present
- [ ] No private keys are present
- [ ] No authentication cookies or session data are present
- [ ] No unredacted sensitive configuration files are present
- [ ] Screenshots have been reviewed for sensitive information
- [ ] Logs have been reviewed before publication
- [ ] Configuration examples use placeholders where appropriate
- [ ] Intentionally vulnerable systems remain isolated
- [ ] Documentation accurately distinguishes lab systems from real external targets

---

## Backups

Repository backups and exported lab configurations should be treated with the same care as the live environment.

Backups may contain:

- Password hashes
- Tokens
- User information
- Configuration secrets
- Certificates
- Network information

Raw backups containing sensitive information should not be stored in this public repository.

Sanitized examples may be published when useful for documentation.

---

## Responsible Disclosure

If you discover that this repository accidentally exposes a real secret, credential, sensitive configuration, or security issue, please avoid reproducing the sensitive information in a public GitHub issue.

Contact the repository maintainer privately through an appropriate GitHub channel when possible.

Non-sensitive documentation errors, broken scripts, and general project issues may be reported publicly.

---

## Security Is Part of the Lab

The goal of Isla Nublar HomeLab is not simply to build systems that work.

The project should demonstrate the ability to:

- Design security boundaries
- Apply least privilege
- Segment networks
- Protect credentials
- Monitor activity
- Detect suspicious behavior
- Recover from failures
- Document risk and remediation
- Learn from mistakes safely

Security decisions will continue to evolve as the lab grows.

---

> **The fences are part of the system.**
