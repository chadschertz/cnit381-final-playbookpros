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