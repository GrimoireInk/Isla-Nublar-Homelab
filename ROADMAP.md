# 🗺️ Isla Nublar HomeLab Roadmap

This roadmap tracks the development of **Isla Nublar HomeLab**, a cybersecurity and infrastructure lab built around the Rosewill THOR V2 chassis.

The project is being developed incrementally around college coursework, technical growth, available budget, and real learning objectives.

---

## Roadmap Philosophy

The lab follows four guiding principles:

- **Student-budget first:** prioritize used, reused, and high-value hardware where practical.
- **Learn before upgrading:** every major purchase should solve a limitation or unlock a new skill.
- **Document everything:** architecture decisions, failures, fixes, configurations, and lessons learned belong in the repository.
- **Keep the lab safe:** vulnerable systems and offensive-security exercises must remain isolated from trusted systems and networks.

---

# Phase 1 — Planning & Architecture 🟡

**Status:** In Progress

### Objectives

- [x] Define the purpose of the homelab
- [x] Select the Rosewill THOR V2 as the primary chassis
- [x] Establish the Jurassic-inspired project theme
- [x] Name the primary server `NUBLAR-CORE`
- [x] Create the GitHub repository
- [x] Create an initial `.gitignore`
- [x] Create the project `README.md`
- [x] Establish a phased, budget-conscious build philosophy
- [x] Keep the Jarvis project separate from NUBLAR-CORE
- [ ] Finalize the initial hardware specification
- [ ] Define the first-build budget
- [ ] Create a hardware inventory
- [ ] Create the initial network architecture diagram
- [ ] Create the initial virtualization architecture diagram
- [ ] Define the initial IP addressing plan
- [ ] Define planned VLAN/security zones
- [ ] Establish documentation standards for the repository

### Deliverables

- `README.md`
- `ROADMAP.md`
- Hardware plan
- Network diagram
- Virtualization diagram
- Initial security model

### Exit Criteria

Phase 1 is complete when the first hardware configuration is selected, documented, and ready to assemble.

---

# Phase 2 — Hardware Assembly

**Status:** Planned

### Objectives

- [ ] Clean and inspect the Rosewill THOR V2
- [ ] Document the chassis condition and available expansion space
- [ ] Install motherboard
- [ ] Install CPU
- [ ] Install CPU cooling
- [ ] Install initial memory
- [ ] Install primary NVMe storage
- [ ] Install initial bulk-storage drive(s)
- [ ] Install power supply
- [ ] Configure case airflow
- [ ] Complete cable management
- [ ] Verify BIOS/UEFI settings
- [ ] Run memory diagnostics
- [ ] Run storage health checks
- [ ] Complete CPU and thermal stress testing
- [ ] Record idle and load temperatures
- [ ] Record approximate power consumption
- [ ] Photograph and document the completed initial build

### Budget Strategy

The initial build should favor practical capacity over flashy hardware. Priority order:

1. Reliable platform
2. Adequate RAM
3. Fast VM storage
4. Reliable power supply
5. Expandable storage
6. Networking upgrades only when needed
7. Dedicated GPU only if a future workload requires one

### Exit Criteria

NUBLAR-CORE passes hardware diagnostics and is stable enough for hypervisor installation.

---

# Phase 3 — Proxmox & Virtualization

**Status:** Planned

### Objectives

- [ ] Install Proxmox VE
- [ ] Configure hostname as `NUBLAR-CORE`
- [ ] Configure management networking
- [ ] Apply updates
- [ ] Configure storage pools
- [ ] Create VM and container templates
- [ ] Test snapshot functionality
- [ ] Test VM backup and restore
- [ ] Establish resource-allocation guidelines
- [ ] Document the Proxmox configuration
- [ ] Create the virtualization architecture diagram

### Initial Virtual Systems

Planned systems may include:

| Name | Purpose |
|---|---|
| `CONTROL-ROOM` | Monitoring and management |
| `HATCHERY` | Container services |
| `GENETICS-LAB` | Linux development environment |
| `VISITOR-CENTER` | Windows Server / Active Directory |
| `RAPTOR` | Offensive-security workstation |
| `PADDOCK-* ` | Isolated cybersecurity targets |
| `GENOME` | Storage/file services |

The final VM inventory will evolve as the lab develops.

### Exit Criteria

NUBLAR-CORE can reliably create, run, snapshot, back up, and restore virtual machines.

---

# Phase 4 — Core Infrastructure

**Status:** Planned

### Objectives

- [ ] Deploy a primary Linux server
- [ ] Deploy Windows Server
- [ ] Build an Active Directory test domain
- [ ] Configure DNS
- [ ] Configure DHCP where appropriate
- [ ] Create administrative and standard user accounts
- [ ] Deploy a Linux development environment
- [ ] Deploy container services
- [ ] Establish centralized time synchronization
- [ ] Begin configuration-management documentation
- [ ] Document core services and dependencies

### Skills Targeted

- Linux administration
- Windows Server
- Active Directory
- DNS
- DHCP
- Identity and access management
- Docker/container administration
- Systems documentation

### Exit Criteria

The lab has a functional base infrastructure suitable for networking and cybersecurity exercises.

---

# Phase 5 — Network Segmentation & Paddocks

**Status:** Planned

### Objectives

- [ ] Add a managed switch when required
- [ ] Define VLAN architecture
- [ ] Create a dedicated management network
- [ ] Create a trusted/general-purpose network
- [ ] Create a development network
- [ ] Create an isolated cybersecurity testing network
- [ ] Create a container/services network where useful
- [ ] Create a future backup network
- [ ] Implement inter-VLAN firewall rules
- [ ] Validate that vulnerable systems cannot reach trusted devices
- [ ] Document firewall rules
- [ ] Document the IP addressing plan
- [ ] Create a final network segmentation diagram

### Planned Security Zones

| Zone | Purpose |
|---|---|
| **CONTROL CENTER** | Infrastructure management |
| **VISITOR CENTER** | General-purpose systems |
| **GENETICS LAB** | Development and research |
| **PADDOCK** | Isolated security-testing environment |
| **HATCHERY** | Containers and experimental services |
| **SITE B** | Future backup infrastructure |

### Exit Criteria

Security zones are segmented, documented, and tested for intended isolation.

---

# Phase 6 — Cybersecurity Lab

**Status:** Planned

### Objectives

- [ ] Deploy Kali Linux
- [ ] Deploy intentionally vulnerable Linux targets
- [ ] Deploy intentionally vulnerable Windows targets
- [ ] Build an Active Directory attack/defense lab
- [ ] Deploy vulnerable web applications
- [ ] Practice reconnaissance in authorized lab environments
- [ ] Practice vulnerability assessment
- [ ] Practice exploitation against owned lab targets
- [ ] Practice privilege escalation
- [ ] Practice lateral movement in isolated environments
- [ ] Practice hardening and remediation
- [ ] Build CTF environments
- [ ] Document attack paths and remediation steps
- [ ] Map selected exercises to MITRE ATT&CK where appropriate

### Safety Requirement

All intentionally vulnerable systems must remain inside authorized, isolated lab environments. Credentials, private keys, tokens, and sensitive configurations must not be committed to the public repository.

### Exit Criteria

The PADDOCK environment supports repeatable offensive and defensive security exercises without exposing trusted systems.

---

# Phase 7 — Monitoring, Logging & Detection

**Status:** Planned

### Objectives

- [ ] Deploy infrastructure monitoring
- [ ] Monitor CPU, memory, storage, and network utilization
- [ ] Create a CONTROL-ROOM dashboard
- [ ] Centralize logs
- [ ] Experiment with Wazuh, Security Onion, or comparable tools
- [ ] Deploy IDS/IPS capabilities where appropriate
- [ ] Create basic alerting rules
- [ ] Generate test security events
- [ ] Validate alert visibility
- [ ] Document detection engineering experiments
- [ ] Track system-health trends

### Possible Tools

- Grafana
- Prometheus
- Wazuh
- Security Onion
- Suricata
- Zeek

Specific tools will be selected based on available system resources and learning goals.

### Exit Criteria

The lab provides centralized visibility into both infrastructure health and selected security events.

---

# Phase 8 — Storage, Backup & Recovery

**Status:** Planned

### Objectives

- [ ] Expand `GENOME` storage as capacity demands increase
- [ ] Define backup retention policies
- [ ] Back up Proxmox configurations
- [ ] Back up critical VM data
- [ ] Test restoration procedures
- [ ] Add SMART/storage monitoring
- [ ] Document recovery procedures
- [ ] Evaluate a separate backup system
- [ ] Build `SITE-B` when budget and hardware availability permit
- [ ] Test recovery from a simulated host failure

### Exit Criteria

Important lab services and documentation can be restored from tested backups.

---

# Phase 9 — Automation & Infrastructure as Code

**Status:** Future

### Objectives

- [ ] Create reusable Bash scripts
- [ ] Create reusable PowerShell scripts
- [ ] Use Python for selected administration tasks
- [ ] Experiment with Ansible
- [ ] Experiment with Terraform where appropriate
- [ ] Automate repeatable VM configuration tasks
- [ ] Create sanitized configuration templates
- [ ] Document automation workflows
- [ ] Add linting/testing for scripts where practical

### Exit Criteria

Common lab deployments and administrative tasks can be reproduced with documented automation.

---

# Phase 10 — Portfolio & Continuous Improvement

**Status:** Ongoing

### Objectives

- [ ] Maintain a build log
- [ ] Document major troubleshooting incidents
- [ ] Add architecture diagrams
- [ ] Add sanitized screenshots
- [ ] Record meaningful upgrades in `CHANGELOG.md`
- [ ] Turn major lab exercises into portfolio case studies
- [ ] Document lessons learned
- [ ] Periodically review security controls
- [ ] Periodically review unused VMs and services
- [ ] Track power and resource efficiency
- [ ] Keep repository documentation aligned with the real environment

### Portfolio Goal

The repository should demonstrate not only *what* was built, but also:

- Why architectural decisions were made
- How security boundaries were designed
- What problems occurred
- How those problems were diagnosed
- What trade-offs were made because of budget or hardware limitations
- What was learned from each phase

---

# Current Priority Queue

1. Finalize the initial NUBLAR-CORE hardware specification
2. Set a realistic first-build budget
3. Create `docs/hardware/hardware-list.md`
4. Create the initial network architecture
5. Define the initial virtualization plan
6. Create `SECURITY.md`
7. Begin the Phase 1 build log

---

## Project Status Legend

- 🟢 **Complete**
- 🟡 **In Progress**
- ⚪ **Planned**
- 🔵 **Future / Optional**
- 🔴 **Blocked**
