# Blue Team Cybersecurity Home Lab Setup
Author: Kellie Hucker

## Overview
This project provides a high-level overview of the design and implementation of my dedicated cybersecurity home lab, built on an Acer workstation to simulate a structured enterprise-style blue team environment. The lab was developed in phases, progressing from foundational virtualization and networking setup to a fully operational security monitoring environment focused on centralized logging, endpoint visibility, detection engineering, and security analysis.

The environment integrates multiple systems and platforms, including Windows, Ubuntu Server, Kali Linux, Wazuh SIEM, and VMware Workstation, to emulate real-world enterprise infrastructure and defensive security workflows. The lab was designed to provide hands-on experience with SIEM deployment, virtual networking, log ingestion pipelines, endpoint telemetry, alert monitoring, and multi-system integration.

In addition to standing up core infrastructure, the project involved troubleshooting real-world operational challenges related to virtual networking, agent communication, log forwarding, Docker-based deployments, and system interoperability. This lab is an active learning environment for blue team operations, security monitoring, incident investigation, and cybersecurity skill development.

### Lab Architecture
                           INTERNET
                               |
                        [ Home Router ]
                               |
                    ---------------------
                    |                   |
               Windows 11 Host      VMware Workstation Pro
                    |
          -----------------------------------------
          |         |         |         |         |
          |         |         |         |         |
     Win10 VM   Ubuntu VM  Ubuntu VM  Kali VM   Win10 VM
      Client      Wazuh     Dashboard  Attacker   Client 2


## Lab Phases
*Note: I have detailed documentation on my personal Confluence site*
### Phase 1: Home Cybersecurity Lab
1. Established the physical and host-level foundation for the lab environment.

### Phase 2: Foundations
1. Configured core infrastructure, virtualization, and system hardening.
  - Windows 11 host system hardened  
  - Virtual machine environment configured  
  - Snapshot system implemented for rollback and testing  
  - External backup strategy established

### Phase 3: Blue Team Core Setup
1. Active Directory lab environment configured for identity-based scenarios 
2. Deployed monitoring, logging, and detection capabilities.
  - Wazuh SIEM deployed and operational  
  - Sysmon installed for endpoint telemetry  
  - Packet capture capability enabled
  - Installed Sysmon for detailed endpoint visibility  
  - Enabled packet capture for network analysis  

## Results:
- Fully operational cybersecurity home lab  
- Centralized logging and monitoring capabilities  
- Endpoint and network visibility established  
- Scalable environment for blue team experimentation  

## Tips:
- Maintain regular snapshots before major changes  
- Validate logging pipelines after updates  
- Monitor system resource usage across VMs  
- Keep backups of critical lab components

## Security Notes
This project is intended for learning, personal security practice, and portfolio demonstration.
