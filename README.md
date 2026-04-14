# Active Directory Simulation – LUKMANBTECH.AI

This project is the deployment of a Windows Server Domain Controller (Active Directory) for a company called **LUKMANBTECH AI**. It includes domain setup, client configuration, OU design, group policies, and access control in an enterprise environment.

\---

## Company Structure

**LukmanbTech AI** is a small IT services firm with the following structure:

* 1 x Windows Server (AD Domain Controller)
* 1 x Windows 8 Client (HR Department)
* 1 x Windows 8PC Client (Digital Marketing Department)

\---

## Project Objectives

* Configure an AD Domain Controller on Windows Server
* Join client PCs to the domain
* Create Organizational Units (OUs)
* Implement basic Group Policies for access control
* Simulate a centralized IT environment

\---

## Network Design

```
Internet
   ↓
Router (Gateway: 10.0.5.1)
   ↓
Switch
 ┌──────┬─────────────┬──────────────┐
 │      │             │              │
Server  PC1 (Win 8)   PC2 (Win 8)
---

|Device|IP Address|Role|
|-|-|-|
|Windows Server|10.0.5.5|AD Domain Controller (DC)|
|Windows 8|DHCP (10.0.5.3)|Client (HR)|
|Windows 8 PC|DHCP (10.0.5.4)|Client (DM)|

\---

## Domain Configuration

* **Domain Name**: `Lukmanbtech.AI`
* **Server Name**: `WIN-IHTF83E8VMF`
* **Static IP**: `10.0.5.5`
* **AD Roles Installed**: AD DS, DNS (DHCP)

\---

## Organizational Units (OUs)

Created using **Active Directory Users and Computers**:

```
Lukmanbtech.AI
├── OU: USA (HR \& DM)
│   └── Users: Lanre.HR
    └── Users: Ade.DM

├── OU: UK (IT, MKT \& SALES)
│   └── Users:

├── OU: AUSTRALIA (CONSULTATION \& FINANCE)
│   └── Users:
```

\---

## Group Policy (GPO)

Created and linked using **Group Policy Management Console (gpmc.msc)**:

* **GPO Name**: `Disable shut down access`
* **Linked to**: OU: USA
* **Policy Configured**:

  * `User Configuration` > `Administrative Templates` > `Start menu and Taskbar` > 
  * Set **"Remove and prevent access to the Shut Down, Restart, Sleep, and Hibernate command"** to **Enabled**

Result: There are currently no power option when Shut Down icon is clicked.

\---

## Screenshots

* [AD Domain Structure] (https://github.com/Lukmon-B/Active-Directory-Simulation-LUKMANBTECH.AI/blob/main/Screenshots/Prohibit_Access_to_Control_Panel.png)
* GPO Editor Screenshot
* PC joined to domain
Result of Shut Down denied access[text](https://github.com/Lukmon-B/Active-Directory-Simulation-LUKMANBTECH.AI/blob/main/Screenshots/Shut_Down_Access_Denied.png)

\---

## Key Takeaways

* Gained practical experience with Windows Server roles and domain setup
* Implemented centralized access control using Group Policy
* Learned how to structure users and departments with OUs
* Applied IAM concepts in a real-world simulated environment

\---

## Author

**Lukmon K. Balogun** 
Cybersecurity Analyst

