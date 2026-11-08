# 🦖 Isla Nublar HomeLab

> **Life finds a way. Infrastructure should be documented.**

## Overview

**Isla Nublar HomeLab** is my personal cybersecurity and infrastructure HomeLab built inside a restored legacy Gateway tower.

The project began as a conventional HomeLab planned around a Rosewill THOR V2 chassis. The design was later revised to use a legacy Gateway system as the foundation for a retro sleeper build. That change expanded the project beyond infrastructure alone: NUBLAR-CORE now includes legacy hardware restoration, chassis engineering, custom fabrication, 3D printing, airflow design, modern PC integration, virtualization, networking, cybersecurity, monitoring, storage, and automation.

The system is being developed incrementally around real learning objectives, available budget, and documented engineering decisions.

The Jurassic-inspired identity is intentionally fun; the underlying architecture and documentation are intended to reflect professional IT and cybersecurity practices.

---

## Primary System

### NUBLAR-CORE

NUBLAR-CORE is the primary physical system for the Isla Nublar HomeLab.

- **Chassis:** Legacy Gateway tower
- **Build style:** Restored retro sleeper / custom case modification
- **Role:** Virtualization and infrastructure host
- **Planned hypervisor:** Proxmox VE
- **Current phase:** Phase 0 — Legacy System Documentation & Chassis Survey

The exterior will preserve the recognizable Gateway character while incorporating a Jurassic-inspired design, including paintwork and custom 3D-printed dinosaur skeletal elements. Modern hardware selection will occur only after the chassis has been fully surveyed and measured.

---

## Project Goals

The project is intended to build hands-on experience with:

- Computer hardware and system integration
- Legacy computer restoration and modification
- 3D printing and custom fabrication
- Virtualization and Proxmox VE
- Linux and Windows Server administration
- Active Directory and identity management
- Networking, VLANs, and firewall policy
- Docker and containerized services
- Cybersecurity testing in isolated environments
- Centralized logging, SIEM, IDS/IPS, and detection engineering
- Infrastructure monitoring
- Storage, backups, and recovery
- Bash, PowerShell, Python, and infrastructure automation
- Technical troubleshooting and incident documentation
- Git/GitHub and professional infrastructure documentation

---

## Infrastructure Naming

| Name | Role |
|---|---|
| NUBLAR-CORE | Primary physical virtualization host |
| CONTROL-ROOM | Monitoring and management |
| HATCHERY | Container services |
| GENETICS-LAB | Linux development and research environment |
| VISITOR-CENTER | Windows Server / Active Directory |
| RAPTOR | Offensive-security workstation |
| PADDOCK | Isolated cybersecurity environments |
| GENOME | Storage services |
| SITE-B | Future backup infrastructure |

Names may evolve as the architecture develops.

---

## Physical Build Concept

The final system will be a modern HomeLab hidden inside a restored Gateway chassis.

Planned physical work includes:

- Full chassis inspection and measurement
- Documentation of the original Gateway hardware
- Safe teardown of legacy components
- Chassis cleaning and restoration
- Compatibility analysis for modern motherboard and PSU standards
- Airflow redesign where required
- Custom brackets, adapters, and drive-bay components
- Jurassic-inspired exterior paintwork
- 3D-printed dinosaur skeletal exterior elements
- Modern storage, networking, and serviceability improvements

Cosmetic modifications must never interfere with cooling, maintenance access, or electrical safety.

---

## Cybersecurity Lab

One of the major purposes of Isla Nublar is to create a safe, isolated environment for cybersecurity experimentation.

Planned environments include Kali Linux, Windows and Linux test systems, Active Directory attack/defense labs, vulnerable virtual machines, web application security labs, SIEM experimentation, intrusion detection, log analysis, penetration-testing exercises, and CTF environments.

Intentionally vulnerable systems will remain isolated from trusted systems through virtualization, network segmentation, and firewall policy.

See [SECURITY.md](SECURITY.md) for the repository and lab security policy.

---

## Documentation Philosophy

This repository is intended to document not only **what** was built, but also **how and why** it was built.

For meaningful changes, documentation should capture:

1. Current state
2. Goal
3. Action performed
4. Result
5. Problems encountered
6. Troubleshooting and solution
7. Design decision
8. Reason for the decision
9. Supporting photographs, diagrams, or configuration
10. Next step

Failures and redesigns are part of the project record rather than something to hide. The goal is a reproducible engineering history.

---

## Current Phase

### Phase 0 — Legacy System Documentation & Chassis Survey

Current work:

- Document the Gateway system before disassembly
- Inventory original hardware and labels
- Photograph the original configuration
- Safely remove legacy components
- Measure motherboard, PSU, drive, expansion, cooling, and front-panel areas
- Determine modern hardware compatibility
- Identify required chassis modifications before purchasing components

See [ROADMAP.md](ROADMAP.md) for the complete development plan.

---

## Repository Structure

Documentation will grow into the following areas as the project develops:

- `docs/00-project-overview/` — project scope and design decisions
- `docs/01-chassis/` — original system, teardown, measurements, and chassis survey
- `docs/02-hardware/` — requirements, inventory, and component selection
- `docs/03-case-mod/` — restoration, airflow, painting, and fabrication
- `docs/04-virtualization/` — Proxmox and VM/container architecture
- `docs/05-networking/` — addressing, VLANs, switching, routing, and firewall policy
- `docs/06-infrastructure/` — Windows, Linux, identity, DNS, DHCP, and services
- `docs/07-security/` — cyber range, logging, detection, and defensive exercises
- `docs/08-monitoring/` — infrastructure and security monitoring
- `docs/09-automation/` — scripts and infrastructure automation
- `docs/10-backup-recovery/` — backup, restoration, and recovery procedures
- `cad/` — custom brackets, mounts, and exterior components
- `diagrams/` — hardware, network, and virtualization diagrams
- `configs/` — sanitized configuration examples
- `scripts/` — reusable administration and automation scripts
- `incident-reports/` — documented troubleshooting and security incidents
- `images/` — photographic build documentation

---

## Jarvis Project

The Isla Nublar HomeLab and my Jarvis development project are separate environments.

**Jarvis is not hosted on NUBLAR-CORE.**

Future integrations may be explored, but Isla Nublar is not intended to serve as Jarvis's primary infrastructure.

---

## Disclaimer

This is an independent educational and fan-inspired project.

Jurassic Park, Jurassic World, and associated trademarks and intellectual property belong to their respective rights holders. This project is not affiliated with or endorsed by Universal Pictures, Amblin Entertainment, or other rights holders.