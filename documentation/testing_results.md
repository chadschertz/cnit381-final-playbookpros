# Testing Results
Here are the results following testing our playbooks. All in all, we saw successful execution of all 7 of the developed playbooks.

# Specific Test Results
## Show Initial Ping Connectivity to Devices
![Screenshot of Initial Ping Connectivity to Devices.](/screenshots/InitialPingTestViaAnsible.png)

## Show Loopbacks Created Automatically
### R1
![Screenshot of show ip interface brief for R1.](/screenshots/R1-IPInterfaces.png)

### R2
![Screenshot of show ip interface brief for R2.](/screenshots/R2-IPInterfaces.png)

## Show EIGRP Neighbor Relationships and EIGRP Routes
### R1
![Screenshot of eigrp neighbors and eigrp routes for R1.](/screenshots/R1-EIGRP.png)

### R2
![Screenshot of eigrp neighbors and eigrp routes for R2.](/screenshots/R2-EIGRP.png)

## Demonstrate Connectivity Between Loopback Interfaces
![Screenshot of pings from R1 to R2 loopback interfaces.](/screenshots/LoopbackInterfaceConnectivity.png)

## Show VLANs
### S1
![Screenshot of show vlan brief for S1.](/screenshots/S1-VLAN.png)

### S2
![Screenshot of show vlan brief for S2.](/screenshots/S2-VLAN.png)

## Show EtherChannel
### S1
![Screenshot of show etherchannel summary for S1.](/screenshots/S1-EtherChannelSummary.png)

### S2
![Screenshot of show etherchannel summary for S2.](/screenshots/S2-EtherChannelSummary.png)

## Show Configured Services (NTP and Logging)
### NTP Configuration
![Screenshot of NTP and Logging configuration.](/screenshots/ServicesConfig.png)

## Show Backups Folder
![Screenshot of the backups folder.](/screenshots/Playbook6-BackupsFolder.png)


---

# General Playbook Results
## 01_verify_connectivity.yaml
### Running the Playbook
![Screenshot of Playbook 1 Commands.](/screenshots/Playbook1-Run.gif)

### Play Recap
![Screenshot of Playbook 1 Play Recap.](/screenshots/Playbook1-PlayRecap.png)

## 02_base_config.yaml
### Running the Playbook
![Screenshot of Playbook 2 Commands.](/screenshots/Playbook2-Run.gif)

### Play Recap
![Screenshot of Playbook 2 Play Recap.](/screenshots/Playbook2-PlayRecap.png)

## 03_eigrp_config.yaml
### Running the Playbook
![Screenshot of Playbook 3 Commands.](/screenshots/Playbook3-Run.gif)

### Play Recap
![Screenshot of Playbook 3 Play Recap.](/screenshots/Playbook3-PlayRecap.png)

## 04_vlan_config.yaml
### Running the Playbook
![Screenshot of Playbook 4 Commands.](/screenshots/Playbook4-Run.gif)

### Play Recap
![Screenshot of Playbook 4 Play Recap.](/screenshots/Playbook4-PlayRecap.png)

## 05_services_config.yaml
### Running the Playbook
![Screenshot of Playbook 5 Commands.](/screenshots/Playbook5-Run.gif)

### Play Recap
![Screenshot of Playbook 5 Play Recap.](/screenshots/Playbook5-PlayRecap.png)

## 06_backup_config.yaml
### Running the Playbook
![Screenshot of Playbook 6 Commands.](/screenshots/Playbook6-Run.gif)

### Play Recap
![Screenshot of Playbook 6 Play Recap.](/screenshots/Playbook6-PlayRecap.png)

## 07_etherchannel_config.yaml
### Running the Playbook
![Screenshot of Playbook 7 Commands.](/screenshots/Playbook7-Run.gif)

### Play Recap
![Screenshot of Playbook 7 Play Recap.](/screenshots/Playbook7-PlayRecap.png)