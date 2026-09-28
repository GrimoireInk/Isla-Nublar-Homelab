🦖 Isla Nublar HomeLab

> **Life finds a way. Infrastructure should be documented.**

## Overview

**Isla Nublar HomeLab** is my personal cybersecurity and infrastructure homelab built inside a customized Rosewill THOR V2 full-tower chassis.

The project is a budget-conscious, to-start, learning environment where I can gain hands-on experience with virtualization, networking, operating systems, cybersecurity, Active Directory, monitoring, storage, and systems administration.

Rather than building the entire environment at once, I'm developing the lab incrementally as my technical skills, requirements, and budget grow.

The Jurassic-inspired naming system gives the project its identity, while the underlying architecture and documentation are designed around real-world IT and cybersecurity concepts. I'm also a huge Jurassic Park fan.

---

## 🎯 Project Goals

The primary goals of the Isla Nublar HomeLab are to:

- Build and administer a virtualization environment
- Gain practical Linux and Windows Server experience
- Create Active Directory environments
- Practice network segmentation and VLAN configuration
- Build isolated cybersecurity testing environments
- Learn firewall administration
- Deploy and manage Docker containers
- Implement infrastructure monitoring
- Experiment with SIEM and security-monitoring technologies
- Develop automation skills with Bash, PowerShell, and Python
- Learn storage and backup administration
- Document infrastructure using professional practices
- Create demonstrable cybersecurity projects for my technical portfolio

---

## 🖥️ Primary System

### NUBLAR-CORE

`NUBLAR-CORE` is the primary physical server hosting the virtualized homelab infrastructure.

**Chassis:** Rosewill THOR V2  
**Role:** Virtualization / Infrastructure Server  
**Hypervisor:** Proxmox VE

The system is intentionally being built with an upgrade-over-time philosophy.

Instead of purchasing enterprise-level hardware immediately, components will be added as new technical requirements emerge.

---

## 🦖 Infrastructure Naming

The lab uses a Jurassic-inspired naming system while keeping the technical purpose of each system documented.

| Name | Role |
|---|---|
| NUBLAR-CORE | Primary Proxmox host |
| CONTROL-ROOM | Monitoring and management |
| HATCHERY | Container services |
| GENETICS-LAB | Linux development environment |
| VISITOR-CENTER | Windows Server / Active Directory |
| RAPTOR | Offensive-security workstation |
| PADDOCK | Isolated cybersecurity environments |
| GENOME | Storage services |
| SITE-B | Future backup infrastructure |

Names may change as the architecture develops.

---

## 🔬 Cybersecurity Lab

One of the major purposes of Isla Nublar is to create a safe, isolated environment for cybersecurity experimentation.

Planned environments include:

- Kali Linux
- Windows test systems
- Linux test systems
- Active Directory labs
- Vulnerable virtual machines
- Web application security labs
- Network-security exercises
- SIEM experimentation
- Intrusion detection
- Log analysis
- Penetration-testing exercises
- Capture-the-Flag environments

Security-testing systems will be separated from trusted systems using virtualization and network segmentation.

---

## 🌐 Planned Network Architecture

The network will eventually be separated into multiple logical security zones.

Examples may include:

**CONTROL CENTER**  
Infrastructure management.

**VISITOR CENTER**  
General-purpose systems.

**GENETICS LAB**  
Development and research.

**PADDOCK**  
Cybersecurity testing and intentionally vulnerable systems.

**HATCHERY**  
Containers and experimental services.

**SITE B**  
Backup infrastructure.

The final VLAN and IP addressing architecture will be documented as the network is built.

---

## 💾 Storage

Storage will initially remain simple and expand as needed.

Planned storage roles include:

- Virtual machine storage
- ISO images
- Project files
- School-related technical projects
- Cybersecurity datasets
- System backups
- Configuration backups
- Documentation
- Lab snapshots

A dedicated storage architecture may be introduced later as capacity requirements increase.

---

## 🗺️ Current Phase

### Phase 1 — Planning & Architecture

Current work includes:

- Hardware planning
- Server architecture
- Naming conventions
- Virtualization planning
- Network planning
- Repository documentation
- Physical system design

---

## 🚧 Planned Development

Future phases are expected to include:

**Phase 2 — Hardware Assembly**

Build and configure NUBLAR-CORE.

**Phase 3 — Virtualization**

Install and configure Proxmox VE.

**Phase 4 — Core Infrastructure**

Deploy management, Linux, and Windows environments.

**Phase 5 — Network Segmentation**

Introduce VLANs and dedicated security zones.

**Phase 6 — Cybersecurity Lab**

Deploy isolated offensive and defensive security environments.

**Phase 7 — Monitoring & Detection**

Introduce centralized monitoring, logging, and SIEM experimentation.

**Phase 8 — Backup & Recovery**

Develop SITE-B backup infrastructure.

---

## 📚 Skills Demonstrated

This project is intended to provide hands-on experience with technologies and concepts including:

`Linux`  
`Windows Server`  
`Active Directory`  
`Proxmox VE`  
`Virtualization`  
`Networking`  
`VLANs`  
`Firewalls`  
`Docker`  
`Cybersecurity`  
`SIEM`  
`IDS/IPS`  
`Bash`  
`PowerShell`  
`Python`  
`Git`  
`GitHub`  
`Infrastructure Documentation`

---

## 🤖 Jarvis Project

The Isla Nublar HomeLab and my Jarvis development project are separate environments.

**Jarvis is not hosted on NUBLAR-CORE.**

Future integrations between the projects may be explored, but Isla Nublar is not intended to serve as Jarvis's primary infrastructure.

---

## ⚠️ Security Notice

Configuration examples published in this repository are sanitized before publication.

Credentials, private keys, authentication tokens, sensitive configuration information, and other secrets will never intentionally be committed to this repository.

Any vulnerable systems documented in this project are operated only within authorized and isolated lab environments.

---

## 📝 Documentation

Detailed documentation can be found within the `/docs` directory as the project develops.

This repository will evolve alongside the physical homelab.

---

## Disclaimer

This is an independent educational and fan-inspired project.

Jurassic Park, Jurassic World, and associated trademarks and intellectual property belong to their respective rights holders. This project is not affiliated with or endorsed by Universal Pictures, Amblin Entertainment, or other rights holders.
