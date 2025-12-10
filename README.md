# CNIT-381 Final Project: Playbook Pros
This is the final GitHub Repository for our CNIT-381 Final Project. We are team Playbook Pros!

# Team Members
Chad S. and Drew A.

# Project Description
The project description will go here. 

# How to Run Each Playbook
## Ansible Host Setup
You will need to have access to an ansible host in your environment to run the playbooks. For the case of this lab, we are utilizng a Windows worksation with Windows Subsystem for Linux (WSL) installed. We are using the Ubuntu distribution.

To install Ansible, perform the following:

```sudo apt update```

```sudo apt install ansible sshpass python3-paramiko -y```

Verify that Ansible has been installed by running the following command:

```ansible --version```

## Commands
| Playbook | Command to Run |
|---|---|
| 01_verify_connectivity.yaml | ```ansible-playbook 01_verify_connectivity.yaml``` |
| 02_base_config.yaml | ```ansible-playbook 02_base_config.yaml``` |
| 03_eigrp_config.yaml | ```ansible-playbook 03_eigrp_config.yaml``` |
| 04_vlan_config.yaml | ```ansible-playbook 04_vlan_config.yaml``` |
| 05_services_config.yaml | ```ansible-playbook 05_services_config.yaml``` |
| 06_backup_config.yaml | ```ansible-playbook 06_backup_config.yaml``` |
| 07_etherchannel_config.yaml | ```ansible-playbook 07_etherchannel_config.yaml``` |

# Summary of Each Playbook
* 01_verify_connectivity.yaml
  * This playbook...
* 02_base_config.yaml
  * This playbook...
* 03_eigrp_config.yaml
  * This playbook...
* 04_vlan_config.yaml
  * This playbook...
* 05_services_config.yaml
  * This playbook...
* 06_backup_config.yaml
  * This playbook...
* 07_etherchannel_config.yaml
  * This playbook...

---
# IP Addressing Tables
## R1
| Device | Interface | IPv4 Address |
|---|---|---|
| R1 | G0/0/0 | 10.99.1.1/30 |
| R1 | Lo1 | 10.1.1.1/32 |
| R1 | Lo2 | 10.1.2.1/32 |
| R1 | Lo3 | 10.1.3.1/32 | 

## R2
| Device | Interface | IPv4 Address |
|---|---|---|
| R2 | G0/0/0 | 10.99.2.1/30 |
| R2 | Lo1 | 10.2.1.1/32 |
| R2 | Lo2 | 10.2.2.1/32 |
| R2 | Lo3 | 10.2.3.1/32 | 

## S1
| Device | Interface | IPv4 Address |
|---|---|---|
| S1 | G1/0/10 | 10.99.1.2/30 |
| S1 | G1/0/11 | 10.99.2.2/30 |
| S1 | VLAN 10 | 10.10.0.1/24 |
| S1 | VLAN 20 | 10.20.0.1/24 |
| S1 | VLAN 30 | 10.30.0.1/24 |
| S1 | VLAN 99 | 10.99.0.10/24 |
| S1 | VLAN 999 | N/A (Native) |

## S2
| Device | Interface | IPv4 Address |
|---|---|---|
| S1 | VLAN 99 | 10.99.0.20/24 |
| S1 | VLAN 999 | N/A (Native) |

# VLAN Table
| VLAN ID | Name | IP Range for VLAN |
|---|---|---|
| 10 | Data | 10.10.0.0/24 |
| 20 | Voice | 10.20.0.0/24 |
| 30 | Cameras | 10.30.0.0/24 |
| 99 | Management | 10.99.0.0/24 |
| 999 | Native | N/A |
