# CIS-System-Security-fall-25-Project

# Active Defense: SIEM Implementation & SSH Hardening

## Mission Statement
[This project implements a 'Purple Team' simulation to address the risks of internal network compromises and lateral movement. By integrating concepts from Module 1 (Threats & Attacks), Module 9 (Security Architecture), and Module 14 (Incident Response), we have designed an isolated security lab using Docker containers. Our team operates as both the attacker—executing active reconnaissance and SSH brute force attacks against a vulnerable gateway—and the defender, utilizing a Wazuh SIEM to detect, log, and analyze these threats in real-time. The objective is to demonstrate the complete lifecycle of a security incident, from initial network scanning to final detection and reporting.]

## Tech Stack
* **Virtualization:** Docker Engine
* **SIEM:** Wazuh (Manager, Indexer, Dashboard)
* **Target:** Ubuntu 22.04 LTS
* **Attack Tools:** Kali Linux (Nmap, Hydra)

## What did we build? (The Architecture)
- The Concept: We built a "SOC in a Box." Instead of needing 3 physical computers, we used Docker to simulate a corporate network inside a single laptop.

- The Components:
  - The Brain (Wazuh SIEM): This is the security center. It collects data, looks for hackers, and generates the alerts we see on the screen.
  - The Victim (Ubuntu Server): This represents an employee's server or a company website. It is the target we are going to attack.
  - The Spy (Wazuh Agent): A small piece of software we installed on the Victim. It acts like a security camera, watching files and network traffic and  sending reports back to the Brain.

- Why did we use Docker?
  - Efficiency: We spun up an entire Security Operations Center (SOC) in minutes rather than hours.
  - Isolation: If we accidentally destroy the "Victim" with malware, it doesn't hurt our real computers. We just delete the container and start a new one.

##  Project Team & Roles

**Nathaniel (Project Lead & System Architect)**
* **Responsibilities:** * Leads the GitHub Project board and sprint management.
    * Deploys the core SIEM infrastructure (Wazuh Docker).
    * Configures network connectivity and endpoint agents.
    * Maintains the repository structure and integration.

**Esai (Red Team Operator & System Administrator)**
* **Responsibilities:**
    * Executes active attacks (Brute Force, Network Scanning) to generate security events.
    * Manages the "Victim" container environment.
    * Assists with agent connectivity testing.

**Asia (Security Analyst & Documentation Lead)**
* **Responsibilities:**
    * Monitors the SIEM dashboard for real-time alerts.
    * Analyzes logs to identify attack signatures.
    * Documents findings, chain of custody, and produces the final Incident Response Report in the Wiki.

    ## Individual Contribution Summary
| Team Member | Role | Story Points Completed |
| :--- | :--- | :--- | 
| [Your Name] | System Architect/Red Team | [10] |
| [Esai] | Red Team | [8] |
| [Asia] | Blue Team Analyst | [7] |
