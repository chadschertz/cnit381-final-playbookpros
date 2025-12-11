# CNIT-381 Final Project: Playbook Pros
This is our final GitHub Repository for our CNIT-381 Final Project. 

We are team Playbook Pros!

# Team Members
Chad S. and Drew A.

# Project Description
This project will automate the network configuration of 2 Cisco Routers and 2 Cisco Switches using Ansible. The playbooks that have been developed will automate the configuration of base settings, EIGRP routing, VLANs, network services, configuration backups, and EtherChannel configuration. In order to execute these playbooks you will need an Ansible host with SSH access to the devices you want to configure. Overall, Ansible proves to be a very powerful tool to automate network configurations and can dramatically decrease configuration time of networking devices. 

# How to Run Each Playbook
## Ansible Host Setup
You will need to have access to an Ansible host in your environment to run the playbooks. For the case of this lab, we are utilizng a Windows worksation with Windows Subsystem for Linux (WSL) installed, with the Ubuntu distribution.

To install Ansible, perform the following:

```sudo apt update```

```sudo apt install ansible sshpass python3-paramiko -y```

Verify that Ansible has been installed by running the following command:

```ansible --version```

## Commands
| Playbook | Command to Run |
|---|---|
| Initial Ping Test Command | ```ansible all -i inventory.ini -m ping``` |
| 01_verify_connectivity.yaml | ```ansible-playbook -i inventory.ini playbooks/01_verify_connectivity.yaml``` |
| 02_base_config.yaml | ```ansible-playbook -i inventory.ini playbooks/02_base_config.yaml``` |
| 03_eigrp_config.yaml | ```ansible-playbook -i inventory.ini playbooks/03_eigrp_config.yaml``` |
| 04_vlan_config.yaml | ```ansible-playbook -i inventory.ini playbooks/04_vlan_config.yaml``` |
| 05_services_config.yaml | ```ansible-playbook -i inventory.ini playbooks/05_services_config.yaml``` |
| 06_backup_config.yaml | ```ansible-playbook -i inventory.ini playbooks/06_backup_config.yaml``` |
| 07_etherchannel_config.yaml | ```ansible-playbook -i inventory.ini playbooks/07_etherchannel_config.yaml``` |

# Summary of Each Playbook
* 01_verify_connectivity.yaml
  * This playbook verifies connectivity to the devices specifed in the ```inventory.ini``` file by printing out its show version information to the console. 
* 02_base_config.yaml
  * This playbook updates the hostname with the device hostname variable specified in the ```inventory.ini``` file, configures interface descriptions as defined in the ```inventory.ini``` file, and sets message of the day login banners on all devices. 
* 03_eigrp_config.yaml
  * This playbook configures an additional 3 loopback interfaces on the router, and then configures EIGRP in AS 100 for the routers. 
* 04_vlan_config.yaml
  * This playbook configures VLANs as specified in the ```inventory.ini``` file. 
* 05_services_config.yaml
  * This playbook configures basic NTP server information and configures logging on each of the devices.
* 06_backup_config.yaml
  * This playbook runs the ```show running-configuration``` command on all devices in the ```inventory.ini``` file and saves this output to the ```backups/``` directory, with the date and time appended to the configuration file's name. 
* 07_etherchannel_config.yaml
  * This playbook automates LACP EtherChannel configuration for the interfaces specified in the ```inventory.ini``` file. It also configures Port-channel1 as a trunk port, and adds Native VLAN information to this. 

---
# Network Topology Diagram
![Screenshot of Initial Ping Connectivity to Devices.](/screenshots/Topology.png)

# IP Addressing Tables
## R1
| Device | Interface | IPv4 Address |
|---|---|---|
| R1 | G0/0/0 | 10.99.0.1/24 |
| R1 | Lo1 | 10.1.1.1/32 |
| R1 | Lo2 | 10.1.2.1/32 |
| R1 | Lo3 | 10.1.3.1/32 | 

## R2
| Device | Interface | IPv4 Address |
|---|---|---|
| R2 | G0/0/0 | 10.99.0.2/24 |
| R2 | Lo1 | 10.2.1.1/32 |
| R2 | Lo2 | 10.2.2.1/32 |
| R2 | Lo3 | 10.2.3.1/32 | 

## S1
| Device | Interface | IPv4 Address |
|---|---|---|
| S1 | VLAN 1 | 10.99.0.10/24 |

## S2
| Device | Interface | IPv4 Address |
|---|---|---|
| S1 | VLAN 1 | 10.99.0.20/24 |

# VLAN Table
| VLAN ID | Name |
|---|---|
| 10 | Data |
| 20 | Voice |
| 30 | Cameras |
| 99 | Management |
| 999 | Native |
