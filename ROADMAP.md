# 🗺️ Isla Nublar HomeLab Roadmap

This roadmap tracks the development of **Isla Nublar HomeLab**, a cybersecurity and infrastructure HomeLab built inside a restored legacy Gateway tower.

The project is developed incrementally around college coursework, technical growth, available budget, and real learning objectives.

## Roadmap Philosophy

- **Student-budget first:** prioritize used, reused, and high-value hardware where practical.
- **Learn before upgrading:** every major purchase should solve a limitation or unlock a new skill.
- **Measure before buying:** the Gateway chassis must be surveyed before modern hardware is selected.
- **Document everything:** architecture decisions, failures, fixes, configurations, measurements, and lessons learned belong in the repository.
- **Keep the lab safe:** vulnerable systems and offensive-security exercises must remain isolated from trusted systems and networks.
- **Preserve serviceability:** exterior modifications must not prevent cooling, maintenance, or safe component replacement.

---

# Phase 0 — Legacy System Documentation & Chassis Survey 🟡

**Status:** In Progress

### Objectives

- [x] Define the purpose of the HomeLab
- [x] Establish the Jurassic-inspired project theme
- [x] Name the primary server NUBLAR-CORE
- [x] Create the GitHub repository
- [x] Establish a budget-conscious build philosophy
- [x] Keep the Jarvis project separate from NUBLAR-CORE
- [x] Revise the physical design from the Rosewill THOR V2 to a legacy Gateway sleeper build
- [x] Capture initial exterior and interior photographs
- [ ] Identify the Gateway model and readable part/model labels
- [ ] Inventory the original installed hardware
- [ ] Document front-panel wiring before disassembly
- [ ] Safely remove legacy expansion cards, drives, motherboard, and PSU
- [ ] Photograph the empty chassis
- [ ] Measure the motherboard tray and mounting pattern
- [ ] Measure the rear I/O opening and expansion slots
- [ ] Measure the PSU bay and mounting-hole pattern
- [ ] Measure CPU-cooler clearance
- [ ] Document 5.25-inch and 3.5-inch drive-bay dimensions
- [ ] Identify front, rear, side, and bottom airflow opportunities
- [ ] Determine whether standard ATX, Micro-ATX, Mini-ITX, ATX PSU, or SFX hardware can be supported
- [ ] Identify required adapters, brackets, drilling, or fabrication

### Exit Criteria

Phase 0 is complete when the empty chassis is documented and measured well enough to select modern hardware without guessing.

---

# Phase 1 — Hardware Architecture ⚪

**Status:** Planned

### Objectives

- [ ] Define compute requirements for planned workloads
- [ ] Define target RAM capacity and upgrade path
- [ ] Define VM/container storage requirements
- [ ] Define bulk-storage and backup requirements
- [ ] Select motherboard form factor based on Phase 0 measurements
- [ ] Select CPU platform based on workload, efficiency, budget, and virtualization support
- [ ] Select a reliable modern PSU
- [ ] Select CPU cooling compatible with chassis clearance
- [ ] Select networking requirements and any add-in NICs
- [ ] Create the initial hardware inventory and budget
- [ ] Document alternatives considered and reasons for final selections

### Exit Criteria

The first modern hardware configuration is selected, documented, compatible with the Gateway chassis, and ready for purchase/assembly.

---

# Phase 2 — Chassis Restoration & Modification ⚪

### Objectives

- [ ] Fully clean the chassis and removable panels
- [ ] Address corrosion, damage, or degraded fasteners if present
- [ ] Preserve the Gateway identity and useful original components where practical
- [ ] Prepare surfaces for paint
- [ ] Modify airflow only after the hardware and thermal plan are defined
- [ ] Adapt motherboard, PSU, storage, and I/O mounting as required
- [ ] Preserve safe side-panel removal and maintenance access
- [ ] Document all irreversible chassis modifications

### Exit Criteria

The restored chassis is structurally ready to accept modern hardware and has a documented cooling and mounting plan.

---

# Phase 3 — Custom Fabrication & 3D Printing ⚪

### Objectives

- [ ] Design required motherboard/PSU/fan/drive adapters
- [ ] Prototype and test custom mounts
- [ ] Design any stealth modern I/O for legacy drive bays
- [ ] Design Jurassic-inspired exterior components
- [ ] Create shallow 3D dinosaur skeletal elements that do not obstruct ventilation
- [ ] Document CAD revisions and print settings
- [ ] Verify printed parts tolerate expected temperature and mechanical loads

### Exit Criteria

Required custom components fit correctly, remain serviceable, and do not compromise airflow or safety.

---

# Phase 4 — Modern System Assembly ⚪

### Objectives

- [ ] Install motherboard, CPU, and cooling
- [ ] Install memory
- [ ] Install primary VM/storage devices
- [ ] Install modern PSU
- [ ] Install networking hardware
- [ ] Complete cable management
- [ ] Configure airflow
- [ ] Verify BIOS/UEFI settings and virtualization support
- [ ] Run memory diagnostics and storage health checks
- [ ] Run CPU and thermal stress testing
- [ ] Record idle/load temperatures and approximate power consumption
- [ ] Photograph and document the completed initial hardware build

### Exit Criteria

NUBLAR-CORE passes hardware diagnostics and is stable enough for hypervisor installation.

---

# Phase 5 — Proxmox & Virtualization ⚪

### Objectives

- [ ] Install Proxmox VE
- [ ] Configure NUBLAR-CORE hostname and management networking
- [ ] Apply updates and document baseline configuration
- [ ] Configure storage pools
- [ ] Create VM and container templates
- [ ] Test snapshots
- [ ] Test VM backup and restore
- [ ] Establish resource-allocation guidelines
- [ ] Create the virtualization architecture diagram

### Planned Virtual Systems

| Name | Purpose |
|---|---|
| CONTROL-ROOM | Monitoring and management |
| HATCHERY | Container services |
| GENETICS-LAB | Linux development and research |
| VISITOR-CENTER | Windows Server / Active Directory |
| RAPTOR | Offensive-security workstation |
| PADDOCK-* | Isolated cybersecurity targets |
| GENOME | Storage/file services |

### Exit Criteria

NUBLAR-CORE can reliably create, run, snapshot, back up, and restore virtual machines.

---

# Phase 6 — Core Infrastructure ⚪

### Objectives

- [ ] Deploy a primary Linux server
- [ ] Deploy Windows Server
- [ ] Build an Active Directory test domain
- [ ] Configure DNS and DHCP where appropriate
- [ ] Create administrative and standard user accounts
- [ ] Deploy container services
- [ ] Establish centralized time synchronization
- [ ] Document services and dependencies

### Exit Criteria

The lab has a functional base infrastructure suitable for networking and cybersecurity exercises.

---

# Phase 7 — Network Segmentation & Paddocks ⚪

### Objectives

- [ ] Define the IP addressing plan
- [ ] Add a managed switch when required
- [ ] Define VLAN architecture
- [ ] Create management, trusted, development, services, security-testing, and backup zones as appropriate
- [ ] Implement inter-VLAN firewall rules
- [ ] Validate that vulnerable systems cannot reach trusted devices
- [ ] Document firewall rules and network diagrams

### Exit Criteria

Security zones are segmented, documented, and tested for intended isolation.

---

# Phase 8 — Cybersecurity Lab ⚪

### Objectives

- [ ] Deploy Kali Linux
- [ ] Deploy intentionally vulnerable Linux and Windows targets
- [ ] Build an Active Directory attack/defense lab
- [ ] Deploy vulnerable web applications
- [ ] Practice authorized reconnaissance, vulnerability assessment, exploitation, privilege escalation, and remediation
- [ ] Build CTF environments
- [ ] Document attack paths and defensive fixes
- [ ] Map selected exercises to MITRE ATT&CK where appropriate

### Safety Requirement

All intentionally vulnerable systems must remain inside authorized, isolated lab environments. Credentials, private keys, tokens, and sensitive configurations must not be committed to the public repository.

---

# Phase 9 — Monitoring, Logging & Detection ⚪

### Objectives

- [ ] Monitor CPU, memory, storage, and network utilization
- [ ] Build CONTROL-ROOM dashboards
- [ ] Centralize logs
- [ ] Experiment with Wazuh, Security Onion, or comparable tooling
- [ ] Deploy IDS/IPS capabilities where appropriate
- [ ] Generate test security events and validate alert visibility
- [ ] Document detection engineering experiments

---

# Phase 10 — Storage, Backup & Automation ⚪

### Objectives

- [ ] Expand GENOME storage as capacity demands increase
- [ ] Define backup retention policies
- [ ] Back up critical configurations and VM data
- [ ] Test restoration procedures
- [ ] Add storage health monitoring
- [ ] Evaluate SITE-B as a separate backup platform
- [ ] Create reusable Bash, PowerShell, and Python tooling
- [ ] Experiment with Ansible and Terraform where appropriate
- [ ] Automate repeatable administrative tasks

---

# Phase 11 — Validation, Portfolio & Continuous Improvement ⚪

### Objectives

- [ ] Maintain a build log and changelog
- [ ] Document major troubleshooting incidents
- [ ] Maintain current hardware, network, and virtualization diagrams
- [ ] Add sanitized screenshots and photographs
- [ ] Turn major lab exercises into portfolio case studies
- [ ] Periodically review security controls and unused services
- [ ] Track power, thermal, and resource efficiency
- [ ] Keep repository documentation aligned with the real environment

### Portfolio Goal

The repository should demonstrate what was built, why decisions were made, how failures were diagnosed, what trade-offs were accepted, and what was learned from each phase.

---

# Current Priority Queue

1. Complete Phase 0 documentation of the original Gateway
2. Inventory and safely remove legacy components
3. Photograph the empty chassis
4. Complete chassis measurements
5. Determine modern form-factor compatibility
6. Identify required custom fabrication
7. Begin Phase 1 hardware requirements only after Phase 0 is complete

## Project Status Legend

- 🟢 **Complete**
- 🟡 **In Progress**
- ⚪ **Planned**
- 🔵 **Future / Optional**
- 🔴 **Blocked**