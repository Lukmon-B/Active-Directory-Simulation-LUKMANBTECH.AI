# Active Directory Simulation – LUKMANBTECH.AI

# Active Directory Simulation – CyberTech Solutions

This project demonstrates the deployment of a **Windows Server Domain Controller (Active Directory)** for a simulated organization, **LUKMANBTECH AI**. It covers domain setup, client integration, OU structuring, Group Policy implementation, and access control in an enterprise-like environment.

---

## 🏢 Company Structure

**LukmanBtech AI** is modeled as a small IT services firm with the following setup:

- 1 × Windows Server (Domain Controller)
- 1 × Windows 8 Client  (HR Department)
- 1 × Windows 8PC Client (Digital Marketing Department)

---

## 🎯 Project Objectives

- Configure an Active Directory Domain Controller
- Join client machines to the domain
- Design Organizational Units (OUs)
- Implement Group Policies for access control (GPOs)
- Simulate centralized identity and access management

---

## 🌐 Network Design

```
Internet
   ↓
Router (Gateway: 10.0.5.1)
   ↓
Switch
 ┌──────┬─────────────┬──────────────┐
 │      │             │              │
Server  PC1 (Win 8)   PC2 (Win 8)
```

| Device           | IP Address | Role                          |
|------------------|------------|-------------------------------|
| Windows Server   | 10.0.5.5   | Domain Controller (AD DS)     |
| Windows 8        | DHCP       | Client (HR Department)        |
| Windows 8 PC     | DHCP       | Client (Digital Marketing)    |

---

## 🖥️ Domain Configuration

- **Domain Name:** `lukmanbtech.ai`
- **Server Name:** `LUKMANBTECH`
- **IP Address:** `10.0.5.5` (Static)
- **Roles Installed:**
  - Active Directory Domain Services (AD DS)
  - DNS
  - DHCP

---

## 🗂️ Organizational Units (OUs)

Structured using **Active Directory Users and Computers (ADUC):**

```
LukmanBtech.AI
├── OU: USA HR Department
│   ├── Lanre.HR
│   └── 
│
├── OU: USA DM Department
│   └── Ade.DM
```

---

## 🔐 Group Policy (GPO)

Configured via **Group Policy Management Console (gpmc.msc):**

- **GPO Name:** `Disable shut down access`
- **Linked To:**  USA OU
- **Policy Path:**
  ```
  Computer Configuration → Administrative Templates → System → Start menu and Taskbar
  ```
- **Setting:**
  - **Remove and prevent access to the shut down, Restart,Sleep, and Hibernate command → Enabled**

**Outcome:**  
There are currently no power option when shut down icon is clicked.

---

## 📸 Screenshots

- [Active Directory Domain Structure](https://github.com/Lukmon-B/Active-Directory-Simulation-LUKMANBTECH.AI/blob/main/Screenshots/OUs_Group_Users.png)
- [GPO Configuration Screenshot](https://github.com/Lukmon-B/Active-Directory-Simulation-LUKMANBTECH.AI/blob/main/Screenshots/Group_Policy_Management.png)
- [Client Joined to Domain](https://github.com/Lukmon-B/Active-Directory-Simulation-LUKMANBTECH.AI/blob/main/Screenshots/Windows_machine_connection.png)
- [Result of Shut Down denied access](https://github.com/Lukmon-B/Active-Directory-Simulation-LUKMANBTECH.AI/blob/main/Screenshots/Shut_Down_Access_Denied.png)


---

## 🧠 Key Takeaways

- Hands-on experience deploying and managing Active Directory
- Implementation of centralized access control using GPOs
- Practical OU design aligned with organizational structure
- Real-world application of Identity and Access Management (IAM)

---

## 👤 Author

**Lukmon K. Balogun**  
Cybersecurity Analyst
