# Enterprise IT Infrastructure Plan – Ai.ra Company
**Course:** ITEP 414 – System Administration and Maintenance  
**Program:** Bachelor of Science in Information Technology  
**Institution:** Laguna State Polytechnic University  
**Instructor:** Prof. John Randolf M. Penaredondo, MIT  
**Author:** Dimples Aira Cordon

---

## Executive Summary
This repository contains the complete IT Infrastructure Plan for Ai.ra Company, a newly established software engineering firm with 20 full-time employees. The document covers organizational profile mapping, enterprise hardware and software inventories, network design with VLAN segmentation, key administration role definitions, infrastructure recommendations, and a personal project reflection.

---

## PART 1: Company Profile

* **Company Name:** Ai.ra Company
* **Nature of Business:** Custom Software Development, Mobile Application Engineering, and SaaS Solutions Provider
* **Office Location:** Laguna State Polytechnic University
* **Target Workforce:** 20 Full-Time Employees across single-floor premises.

### Vision Statement
To be a premier software engineering hub in Southeast Asia, empowering businesses through secure, scalable, and innovative digital solutions.

### Mission Statement
ABC Startup Solutions delivers enterprise-grade software products by fostering collaborative engineering practices, maintaining strict operational security, and leveraging modern IT infrastructure.

### Organizational Structure & Employee Distribution

| Department | Headcount | Key IT Requirements |
| :--- | :--- | :--- |
| **Information Technology (IT)** | 5 | High-performance workstations, double monitors, virtualization support, administrative access. |
| **Human Resources (HR)** | 4 | Mobile productivity laptops, secure file access, confidential printing privileges. |
| **Finance** | 5 | Dedicated desktop units, dual displays, access to accounting software, high data redundancy. |
| **Sales** | 6 | Portability, long battery life, remote access tools, cloud CRM software. |
| **TOTAL** | **20** | **1 Enterprise Server, Managed Network, Centralized Security.** |

---

## PART 2: Enterprise Hardware Inventory

| Asset ID | Hardware Category | Item Description / Model Spec | Qty | Department | Primary Purpose & Justification |
| :--- | :--- | :--- | :--- | :--- | :--- |
| `HW-DESK-01` | Desktop Workstation | Dell OptiPlex 7010 (Intel i7, 32GB RAM, 1TB NVMe SSD) | 5 | IT | Heavy compiling, local virtualization, and software engineering. |
| `HW-DESK-02` | Desktop Workstation | Dell OptiPlex 5010 (Intel i5, 16GB RAM, 512GB NVMe SSD) | 5 | Finance | Financial modeling, dual-monitor data processing, data reliability. |
| `HW-LAP-01` | Laptop Workstation | Lenovo ThinkPad E14 (Intel i5, 16GB RAM, 512GB SSD) | 4 | HR | On-site interviews, confidential record management, and mobility. |
| `HW-LAP-02` | Laptop Workstation | Lenovo ThinkPad E14 (Intel i5, 16GB RAM, 512GB SSD) | 6 | Sales | Client presentations, remote work capabilities, field travel. |
| `HW-SRV-01` | Enterprise Rack Server | Dell PowerEdge R450 (2x Intel Xeon 4310, 64GB ECC RAM, RAID 10 4x 2TB SAS) | 1 | Server Room | Runs Active Directory, DNS, DHCP, file storage, and internal Docker registries. |
| `HW-RTR-01` | Enterprise Router | MikroTik Cloud Router Switch CCR2004-16G-2S+ | 1 | Network Rack | Handles WAN routing, inter-VLAN routing, and traffic management. |
| `HW-SW-01` | Managed PoE+ Switch | Cisco Catalyst 1000 48-Port GbE PoE+ (370W) | 1 | Network Rack | Core connectivity for workstations, server, access points, and printers. |
| `HW-WAP-01` | Wireless Access Point | Ubiquiti Unifi AP AC Pro | 2 | Office Floor | Delivers dual-band Wi-Fi connectivity for laptops and mobile devices. |
| `HW-NAS-01` | Network Attached Storage | Synology DiskStation DS923+ (4x 4TB NAS Drives in RAID 5) | 1 | Server Room | High-capacity automated daily local backup storage. |
| `HW-EXT-01` | External Backup Drive | Western Digital Elements 5TB Rugged Portable HDD | 2 | System Admin | Off-site physical cold backups rotated weekly. |
| `HW-MON-01` | Display Monitors | Dell 24" Professional IPS FHD Monitors (P2422H) | 20 | IT & Finance | Dual-monitor configuration for administrative and coding productivity. |
| `HW-PRN-01` | Multi-Function Printer | HP LaserJet Enterprise MFP M428fdw | 1 | Common Area | Secure printing, scanning, and document handling. |
| `HW-UPS-01` | Online Rackmount UPS | APC Smart-UPS SRT 3000VA 230V | 1 | Server Room | Uninterruptible power supply protecting core server rack equipment. |
| `HW-UPS-02` | Desktop UPS Units | APC Back-UPS 650VA | 10 | IT & Finance | Short runtime protection to safely save work during unexpected power cuts. |

---

## PART 3: Enterprise Software Inventory

| Software Name | Version | License Type | Department | Purpose & Justification |
| :--- | :--- | :--- | :--- | :--- |
| **Windows 11 Pro** | 23H2 | Commercial OEM / Volume | All | Standard OS providing BitLocker encryption and domain join capabilities. |
| **Ubuntu Server** | 24.04 LTS | Open Source (GPL) | Server Room | Server OS for virtual machines, application hosting, DNS, and microservices. |
| **Microsoft 365 Business Standard** | Latest Cloud | Commercial Subscription | All | Office tools (Word, Excel, PowerPoint), Exchange email, Teams, and OneDrive. |
| **Visual Studio Code** | 1.88+ | Open Source (MIT) | IT | Standard lightweight IDE for software development and administrative scripting. |
| **Git** | 2.44+ | Open Source (GPL v2) | IT | Distributed version control system for source code tracking. |
| **GitHub Desktop** | Latest | Open Source (MIT) | IT | Graphical interface for developers to manage GitHub repositories efficiently. |
| **Oracle VM VirtualBox** | 7.0+ | Open Source (GPL v3) | IT | Sandbox virtualization tool for testing isolated Linux environments locally. |
| **Google Chrome** | Latest | Freeware | All | Web browser managed centrally via Group Policy. |
| **Microsoft Defender for Endpoint** | Enterprise | Commercial Subscription | All | Enterprise endpoint protection, threat detection, and malware prevention. |
| **AnyDesk Enterprise** | 8.0+ | Commercial Subscription | IT / Helpdesk | Remote desktop utility for internal technical support. |
| **7-Zip** | 23.01 | Open Source (GNU LGPL) | All | File compression and archive utility across all workstations. |

---

## PART 4: Enterprise Network Inventory

| Equipment Name | Quantity | Category | Model / Specification | Network Role |
| :--- | :--- | :--- | :--- | :--- |
| **ISP Modem** | 1 | WAN Gateway | Fiber ONT Modem (Provided by ISP) | Demarcation point converting optical signals for primary internet uplink. |
| **Enterprise Router** | 1 | Edge Routing | MikroTik CCR2004-16G-2S+ | Directs internet traffic, manages subnets, and handles inter-VLAN routing. |
| **Next-Gen Firewall** | 1 | Security Gateway | Fortinet FortiGate 60F | Deep packet inspection, intrusion prevention (IPS), and VPN hosting. |
| **Managed Core Switch** | 1 | Switch | Cisco Catalyst 1000 48-Port PoE+ | Connects wired endpoints, processes VLAN tags, and supplies PoE to WAPs. |
| **Wireless Access Points** | 2 | Wireless Network | Ubiquiti UniFi AP AC Pro | Delivers enterprise Wi-Fi mapped to isolated departmental VLANs. |
| **Patch Panel** | 2 | Cabling | 24-Port Cat6 Unshielded Patch Panel | Consolidates structured cabling runs from office plates into the network rack. |
| **Cat6 Ethernet Cables** | 1 Box (305m) | Wiring | AMP Netconnect Cat6 UTP Cable | High-speed copper cabling supporting 1Gbps throughput across the office. |
| **RJ45 Connectors** | 1 Box (100pcs) | Connectors | Cat6 Shielded Modular Plugs | Crimp connectors used for custom patch cables and wall terminations. |

---

## PART 5: Enterprise Network Diagram
